---
title: "Things I learned at droidcon Berlin 2018"
date: 2018-07-03T00:00:00+01:00
---

![Picture of Android robot with birthday hat on](/images/blogs/droidcon/header3.jpeg)
*Happy 10th birthday, droidcon Berlin!*

This year was droidcon Berlin’s 10th birthday and I enjoyed three days packed with all things Android. In this post, I am sharing my experience and the things which stood out to me the most.

<!--more-->

## Day 1

Day 1 was barcamp-inspired. As well as talks decided on the day, there were some pre-scheduled panel discussions. I liked the room set-up, with some rooms available with traditional conference set-up, but also having a room with tables for workshops and a room with chairs in a circle for more conversation-based sessions.

The first session I attended was **“Sketchnoting”** workshop. This was a big hit last year, and having missed that session, I was very happy to learn this year! Looking forward to learning more things and making my sketchnotes prettier in the future.

{{< tweet 1011183530712420352 >}}

It was interesting hearing the **“Rx must DIE!?”** panel. In my opinion RX is a nice tool, however it has big downfalls. The learning curve is very steep and for most apps it’s a bit of an overkill. As such, I would consider carefully before adding it to the app.

I also attended **“Accessibility Android”** session. While there was only one person in the room actively focusing on accessibility, the room was full of people wanting to improve. The discussion was mainly about vision-related accessibility, such as making sure [TalkBack](https://www.androidcentral.com/what-google-talk-back) works, testing font sizes, making sure [contrast](https://webaim.org/resources/contrastchecker/) is not too low, etc., as well as using the [Accessibility Scanner app](https://play.google.com/store/apps/details?id=com.google.android.apps.accessibility.auditor) to find common issues.

We need to think about other accessibility needs as well; for example, if your app does route finding, does it have a no stairs option? How about someone using the app one-handed, is it still easy to access all the options?

If you need another reason to improve accessibility, making the app easier to use for user with accessibility needs will help every user — known as the [Curb Cut Effect](https://medium.com/@mosaicofminds/the-curb-cut-effect-how-making-public-spaces-accessible-to-people-with-disabilities-helps-everyone-d69f24c58785). I know I am going to push harder for making the apps I work on more accessible in the future.

![Sign leading to droidcon](/images/blogs/droidcon/droidcon_sign.jpeg)

The next panel was **“Women in tech”**, talking about recruiting, importance of diversity and how to create more diverse teams. A lot of discussion was about recruiting, however, with many women quitting tech completely, that is also an important aspect to focus on. Training managers to recognise unconscious bias was mentioned, which would be a great start. Even better, let’s educate all members of the team! A lot of focus was also on women specifically, however, members of other under-represented groups would make great additions to diverse teams and we need to have discussions about how to make sure they are included as well.

Sadly, the room was very empty compared to some other talks. It would be interesting to hear the reasons why so many conference attendees skipped this panel. The tech industry is very male-dominated and we cannot fix the problems with diversity without getting the guys involved, they should be part of the change as well, in making work environments more welcoming to everyone. However, we cannot have this discussion if the people who are needed are not even in the room.

## Day 2

Scheduled talks started on day 2! I was really happy to find out there were two apps with the schedule as the website was very hard to navigate this year, especially on mobile. It looks like the responsive web is not there just yet and we do need native apps after all! :)

I continued with sketchnoting and the first talk I sketched was **“Abstracting the map”**. It’s always a good idea to abstract third-party libraries, so it’s easy to replace in case pricing model changes, etc., but, with maps, it’s often the case of apps getting very tightly coupled with the chosen map provider. Next time I am working on a map, I will use the approach I learned in this session and make sure I have an abstracted solution which will not cause headaches in case the map provider needs to change.

{{< tweet 1011553020839190529 >}}

**“Hacking growth”** was another great talk. I am looking forward to using these tips and experimenting more. One experiment at a time quickly adds up to create growth and good user experience — and you learn things you would not have considered!

{{< tweet 1011559205642358784 >}}

**“The curious case of Android button”** — what does a button even do? Evidently, not that much! This talk improved my understanding of Android styles and I feel ready to take on creating a nice and consistent application theme! :)

{{< tweet 1011591502248796160 >}}

I also enjoyed **“Debunking myths about the deep links”** talk. I have learned some new ways to use deeplinking which I never considered before and learned about limitations.

{{< tweet 1011609141654278145 >}}

![Deeplinking implementations and their limits](/images/blogs/droidcon/deeplinks.jpeg)

## Day 3

Day 3 started with a great keynote from GitLab titled **“The best apps are built in pyjama-pants”** about their process based on the way open source projects work. They have even open sourced the way their company [works](https://about.gitlab.com/handbook/)! A lot of lessons here, especially in regards to documentation and open communication. I do believe that remote working is the future, and we need to have the right processes in place to make it happen — we can even just fork GitLab’s!

Next talk was **“Common poor programming practices and how to avoid them”**. Things to avoid when starting the next project for sure! Sometimes we rush to start implementing things, but taking some time to consider architecture can save so much time later on when the codebase needs to be maintained.

We also had a chance to share our thoughts about the **droidcon developer community**. It’s great to have a chance to give early feedback and I am excited to see what happens with this.

One of the most memorable talks of the conference was **“The Authentic Developer”** by Anastasia Lopez. Soft skills contribute so much to our own well-being and that of our co-workers as well. I would love to see more talks like this one in mobile conferences.

{{< tweet 1011913023496359936 >}}

## Overall

While I have seen a lot of awesome talks, I did miss some others. It’s great that everything is recorded — I am looking forward to catching up online. With as many as 5 talks happening all at once it’s not possible to see everything, so learning is not over just yet :)

I am looking forward to applying the things I learned. I will definitely sketchnote at the conferences I go to, try to experiment more often and I would love to focus more on accessibility and great user experience in the future.

## Notes

This post has been previously published in [Medium](https://medium.com/@sigute/things-i-learned-at-droidcon-berlin-2018-e014d78dde0).
