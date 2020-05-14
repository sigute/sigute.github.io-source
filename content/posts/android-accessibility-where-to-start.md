---
title: "Android Accessibility - Where to start?"
date: 2020-02-11T00:00:00+01:00
---

![Question mark](/images/blogs/accessibility/header_where_to_start.jpeg)

Making sure as many people as possible can use an app you are developing is so important for many of us. If you are just starting to think about accessibility in your Android app, it can be hard to understand what the requirements are and how to get started. This article will allow you to start exploring common accessibility issues in Android apps; making these small improvements will help many users of your app.

<!--more-->

## Tools

The main tools used for Android accessibility testing are offered by Google and many come pre-installed on every device. The main ones you need to start with are:

### Talkback

Most devices have either [Talkback](https://support.google.com/accessibility/android/answer/6283677?hl=en) or a similar screen reader already pre-installed. Once enabled, a tutorial is provided so you can learn how to navigate. With Talkback, captions can be enabled in the settings and are helpful to verify the announcements, and if you need to take a screenshot to share with other members of the team this is a useful feature.

Enable Talkback and captions:

`Settings -> Accessibility -> Talkback -> Settings -> Developer Settings -> Display speech output`

### Accessibility Scanner

[Accessibility Scanner](https://play.google.com/store/apps/details?id=com.google.android.apps.accessibility.auditor) is a tool made by Google specifically for finding common accessibility issues and is very easy to use. It can be downloaded and installed from the Play store. Once installed, any screen in any app can be scanned for issues.

### Contrast checker

After finding issues, sometimes tweaking colours is enough to resolve them. There are many contrast checkers available, I like the [WebAIM](https://webaim.org/resources/contrastchecker/) one as it checks both text and other elements.

## 5 places to start

My advice is to start with these areas to address the most common issues found in many apps. When we think about accessibility in apps, we often think about vision impairments, including vision loss. Another area to think about is mobility impairments which can make it difficult to use controls and navigation.

### Labels and content descriptions

Launch Talkback and start checking what announcements are made as you focus on various views in the app. Some questions to keep in mind while testing:

- Do buttons have labels?
- Do images have content descriptions?
- Do labels match what is actually shown on the screen?
- When the element state changes, is the content description updated? (for example, ticked and unticked radio button)
- Are there some elements which are only decorative and should not be announced?

Fixing issues in this category is usually straightforward. Content description can be added and updated. Decorative elements can be labelled as not important for accessibility and will be skipped. Android Lint provides some warnings for missing accessibility features, and addressing these will help.

The aforementioned Accessibility Scanner will catch a lot of these issues too.

### Navigation

Talkback is the tool to use for this category. Keyboard navigation follows similar paths, so it could be used for testing as well. 

- As you navigate through the app, does focus jump around or is the order followed logical?
- Do you lose focus and need to start at the top of the page again?
- Can all areas be accessed without tapping on the screen directly?
- Does Talkback focus on each element separately or can some elements be grouped? (for example, user name could be navigated as "Name", "Surname" or as one "Name Surname" element)

Fixing navigation can be challenging, so deciding on the strategy early rather than trying to retrofit the solution later is often the best approach. Some things to look into for this category include the accessibility traversal order, setting content descriptions on groups rather than individual items and requesting focus manually on specific elements in some scenarios.

### Font sizes

Changing font to a larger size in device settings will help to check for issues in this area. Display size can be changed as well and should be tested. Things to look for include:

- Does all the text in the app respond to device setting font size?
- Do any elements overlap each other?
- Is any text cut off and cannot be read anymore?

To fix issues in this area, look for any usages of `dp` instead of `sp` for text sizing. Make sure elements scale to match the text sizes and prefer scrollable screens which can accommodate additional height if needed. For the individual views, it is best to avoid fixed height and width. Setting the view height and width to `wrap_content` and using `minWidth` and `minHeight` attributes will help with the scaling.

### Contrast

Contrast can be checked using Accessibility Scanner and other contrast checker tools. It might be hard to determine contrast ratio just by looking. Some questions you might ask are:

- Are any colours very similar to each other?
- Can tappable elements be easily distinguished?
- Is there a rule for what colours of background and text could be used in the app, to make the contrast ratio more predictable?

General requirement is minimum `4.5:1` contrast ratio of text to background, and `3:1` for controls. Outlines can help to distinguish tappable elements in some cases.

### Tap target sizes

If you ever tried tapping a button multiple times without success, you have ran into this issue. Accessibility Scanner will highlight the areas which are too small to tap accurately. Some things to keep in mind include:

- Is there enough padding to tappable elements?
- Are there a lot of small elements right next to each other, so it's easy to mis-tap?
- Can the entire element be tapped or is the tap area limited to a small portion of it?
- Can the tap area be expanded?

Android recommendation is a minimum `48x48dp` for tappable areas. Some margins between elements, where possible, can also make for a nicer experience.

## Watch out for…

### Custom views

If you define your own custom views, be careful. Default Android framework elements come with a lot of built-in accessibility support. Where possible, extending the framework class, like `Button`, might help to reduce some work vs extending a more generic class, such as `FrameLayout`, and having to build various states and announcements from scratch.

## Continue with…

Checking for these common issues will help to improve accessibility in your app. However, there are more things to consider to provide a great experience for users with accessibility needs. [WCAG guidelines](https://www.w3.org/WAI/standards-guidelines/wcag/) are a great place to go for understanding additional requirements and exploring common solutions.

## Notes

Header image: Question mark by [pixabay.com](https://www.pexels.com/photo/ask-blackboard-chalk-board-chalkboard-356079/)

This post has been previously published in Android@Microsoft [Medium](https://medium.com/android-microsoft/android-accessibility-where-to-start-b7875045d9) publication and [dev.to](https://dev.to/sigute/android-accessibility-where-to-start-40ce).
