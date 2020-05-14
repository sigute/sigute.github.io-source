---
title: "Things I learned at droidconDE — Part 1"
date: 2017-09-11T00:00:00+01:00
---

![Droidcon banner](/images/blogs/droidcon/header.jpeg)

I am back home from an intense three day conference. It was a great experience and I learned a lot about persistence, building at scale and Kotlin. This is my overview of technical things I learnt. Soft skills article and general conference overview is [here](/posts/things-i-learned-at-droidcon-de-part-2)!

<!--more-->

## SQLite is over?

From the first day of Barcamp, there were many talks about persistence. Sqlite has been my go-to solution previously. However, it comes with some problems, especially updates are a bit painful and SQL queries are not easy to debug. I really enjoyed the SQL lovers & haters panel.

I am going to try something different when I need a persistence solution next time and I will look at [Room](https://developer.android.com/topic/libraries/architecture/room.html), [Realm](https://realm.io/) and [ObjectBox](http://objectbox.io/). I am especially interested in trying Realm and ObjectBox, as they move away from SQL. Room looks like an interesting solution from Google, but it still involves writing some SQL queries.

## Developing at big scale

One of my favourite talks was from Facebook — “Scaling Android @ Facebook” by Marco Cova. The scale Facebook operates in is hard to comprehend! These are a few key things which stuck with me.

**Why not just develop on master?** All code is on the same mono repo. With many developers working on the same code base, merges become very painful — if you work on your branch for a week, chances are good that code has changed on master in the meanwhile and you are going to struggle merging it back in. With very advanced feature switching, it makes more sense to put the new code behind a feature switch and develop directly on master. No one is going to see the changes until the feature is ready anyway! This is not something I am going to apply here at Base. With smaller team, merge conflicts are rarely painful. However, at Facebook scale this makes perfect sense! It also means that code reviews are smaller and faster.

Facebook releases **new features every week**. How do they achieve this? Master is branched for release every week. This starts a week of stability while the app is in the hands of beta users. A new beta update is released every day with any bug fixes. Oh, also, that’s **2.5 million** of beta users!

There is also alpha group with **100K** users. Alpha users get updates every week directly from master branch, meaning any bugs/regressions can be spotted very quickly before the app goes out to beta.

And one more thing from Facebook… localisation.

![Slide showing localisation in Facebook with 70 languages and 40 MB worth of content](/images/blogs/droidcon/localisation.jpeg)

Localisation quickly turns into a problem when your translation files add up to **40Mb**! (6000+ strings in 70+ languages). Solution: start with English as default and download only required language resources when the app starts. This also requires extension of Android Resources files.

Another talk I really enjoyed was from Realm — “Tales from the dark side: developing SDKs at scale” by Kenneth Geisshirt. Similarly, the talk was also about what happens with scale. There are some weird problems you run into when your userbase grows and the bugs from all the weird and wonderful devices start coming in.

Some of the problems are caused by the bugs which have been long resolved by manufacturers or Android. However, of course, there are no updates on these devices, so you have to either live with your SDK/app being broken on these devices or try to find workarounds. Sometimes this involves looking at and modifying some very low level code.

![Slide showing some memmove code, from article below](/images/blogs/droidcon/low_level_code.jpeg)

Full story [here](https://academy.realm.io/posts/when-memmove-fails/), recommended reading! :)

## Kotlin everywhere!

Majority of code examples used in talks were in Kotlin and it seems like it’s definitely becoming very very popular in Android community. I have not made the change just yet. However, with official support from google, the reasons not to switch are disappearing quickly. After the conference, I feel much more strongly about starting to use Kotlin at work.
There was a good point made during Barcamp that newcomers to Android are likely to start with Kotlin. After a few years, will we be struggling to find new developers who actually want to work on a project with java code base?
And with this, that’s main technical things I learned this year. Thanks for the great experience, maybe I will be back next year as well! :)

## Notes

This post has been previously published in [Medium](https://medium.com/@sigute/things-i-learned-at-droidconde-part-1-f8df64aa0866).
