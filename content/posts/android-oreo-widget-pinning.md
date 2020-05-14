---
title: "Android Oreo widget pinning"
date: 2017-11-17T00:00:00+01:00
---

![Screenshot from the phone showing examples of various widgets](/images/blogs/widgets/header.png)

Widgets — love them or hate them? Either way, Android Oreo APIs make widgets more discoverable and easier to add by pinning a widget to home screen straight from the app. I ran into a few issues with the widget pinning implementation, this article is me sharing what I found out and how I got there at the end.

<!--more-->

*Note: originally published Nov 17, 2017 and code updated to latest libraries Jan 8, 2020. No widget configuration changes were needed for the update!* 😊

I also took this as a chance to give Kotlin a test drive. Full source code is available [here](https://github.com/sigute/WidgetsDemo).

## Setting up success callback

Let’s start with documentation. You might be here because you have tried using official documentation and noticed that the following example does not work

{{< gist sigute 357a5ae5044c3bec38bc5f4c0c6e4b0a >}}

It did not work for me either! It’s unclear what goes into the callback Intent and a method to create PendingIntent does not actually exist. Via some trial and error, I have reached the following working solution:

{{< gist sigute a5c6f5291ae48f78fcf1de8d23e6d500 >}}

I have replaced createBroadcast with existing method getBroadcast.

Callback Intent which is being placed into PendingIntent needs to be for your implementation of BroadcastReceiver. BroadcastReceiver will get widget ID in the onReceive callback if widget is placed successfully. If the user cancels the widget pinning prompt without adding widget, the receiver will not be called.

BroadcastReceiver onReceive implementation looks as follows:

{{< gist sigute 1c3f4070fbd48be4a1590de666805086 >}}

This got me to the point of pinning a widget and receiving widget ID after the widget has been pinned.

## Passing some values to the success callback

But wait! Widget ID alone was not enough for my specific use case. If it is for yours — skip this section! :)

Normally when user added a widget through homescreen, I would launch a configuration activity and save some values as well as the widget IDso the widget can be updated. I added these extra arguments up front to the callback intent for pinned widget. Arguments need to go into a bundle.

{{< gist sigute cf44f1ef8e00a82299e14120cb80c833 >}}

Then these are extracted together with widget ID in BroadcastReceiver. This allowed me to save the data once the widget is successfully added.

{{< gist sigute 466442934c1c4a28cc1616573fd8938d >}}

## Customising widget preview

With the implementation so far, when the widget pinning request is displayed, it shows the widget preview image as the preview. This might be perfectly fine for the use case — I wanted to customise the preview. RemoteViews need to be passed in the pinning request to achieve this.

RemoteViews are created in the exactly same way as they would normally be in AppWidgetProvider. Then the views need to be placed in a bundle with EXTRA_APPWIDGET_PREVIEW value. I replaced the null with newly created bundle with remote views:

{{< gist sigute d1e0c6bb5ebb3c1374bc21eb440ec804 >}}

And one more thing… Newly created widget is not updated straight away — depending on the use case, this might be fine or it might be an issue if the widget is supposed to be showing some specific data. I wanted to show a widget name on the widget in this case. Widget update needs to be triggerred in BroadcastReceiver after saving widget values to update the widget. Widgets can be updated as follows. This code triggers an update of every single widget of this type, but it can be easily customised by passing in only a specific widget ID.

{{< gist sigute 6a137642c39bf9a71a4e568a734540ab >}}

And here is a finished product! :)

![Screenshot from the phone showing widget pinning window](/images/blogs/widgets/widget1.png)

![Screenshot from the phone showing widget on the homescreen](/images/blogs/widgets/widget2.png)

It took me awhile to figure out the right process for setting up the widgets — I hope I made it slightly less painful for you! Please see the [full project](https://github.com/sigute/WidgetsDemo) in github — you can run the demo app and see how it all works together and the additional checks to make.

## Notes

This post has been previously published in [Medium](https://medium.com/@sigute/android-oreo-widget-pinning-in-kotlin-398d529eab28).
