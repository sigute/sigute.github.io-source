---
title: "Why I love working with Kotlin"
date: 2018-07-16T00:00:00+01:00
---

![Hand-drawn heart](/images/blogs/kotlin_love/header.jpeg)

I have been using Kotlin for about a year now, and also started using [Kotlin Android Extensions](https://kotlinlang.org/docs/tutorials/android-plugin.html) recently. These are a few of my favourite Kotlin things!

<!--more-->

## Data classes + Parcelize

Most Android apps I have worked on needed to fetch data from the network, which means writing a lot of models. This is not the exciting development work anyone really wants to do. Kotlin makes this task a lot less tedious.

[Data classes](https://kotlinlang.org/docs/reference/data-classes.html) allow implementing data models in just a few lines. [Parcelize](https://kotlinlang.org/docs/tutorials/android-plugin.html#parcelable) from Kotlin Android Extensions adds Parcelable in just one annotation!

With Java, a simple object model with Parcelable implementation would look something like this:

{{< gist sigute 50365676c18e3fbb4febd1a041c37d7c >}}

Kotlin and Parcelize make all of this possible in only 2 lines.

{{< gist sigute d6fba36291580699d137db7df5195826 >}}

I have also made use of the [JsonToKotlinClass](https://github.com/wuseal/JsonToKotlinClass) Android Studio plug-in recently, which made the process even easier.

## Null handling

A very common app crash — something was null and it was not expected to be. Nullable annotations in Java do help with this. Kotlin does even better by making everything non-null by default. Assigning null leads to the compilation error, forcing the situation to be handled straight away and preventing runtime crashes.

Where null is possible, safe calls make the null checking much less verbose.

{{< gist sigute ec97eab5f0b8386f6805c2057f78b5b0 >}}

{{< gist sigute 93fed543bc340e9e12941c16afebd891 >}}

## findViewById is gone!

Another great Kotlin Android Extension, enabling the use of identifiers defined in XML directly, rather than using findViewById, or adding extra code using some data binding solution. Less code makes it easier to focus on important elements.

{{< gist sigute ae63aa4d08bf1c260b2e64369e09fcf2 >}}

{{< gist sigute 62ad252d6ea453e00260637267d1673d >}}

## Easy migration from Java

Java and Kotlin integrate into the same project easily. This allows the migration to be handled in stages, by package or feature, without the pressure to convert the entire codebase in one go.

## Overall

Kotlin makes Android development more pleasant. At the moment migration is in progress in a lot of companies, so Java code is still here to stay for a bit longer. My preference is definitely for Kotlin projects, and I would be hesitant to use Java only, having seen the benefits of Kotlin!

I ❤ Kotlin!

## Notes

Header photo by [pixabay.com](https://pixabay.com/en/notebook-address-book-point-sketch-2247351/).

This post has been previously published in [Medium](https://medium.com/@sigute/why-i-love-working-with-kotlin-a0001a302dc9).
