---
title: "Things I learned at droidconDE — Part 2"
date: 2017-09-11T00:01:00+01:00
---

![Picture shows the stage named for Hedy Lamarr](/images/blogs/droidcon/header2.jpeg)

This is general overview of my experience at Droidcon, including soft skills I learned! Part 1 with more technical things I learned can be found [here](/posts/things-i-learned-at-droidcon-de-part-1).

<!--more-->

Having arrived in Berlin a few days before the conference, I was there nice and early for Barcamp on Sunday morning. The first thing to catch my eye were stage names. Droidcon was happening across 4 stages — named after [Hedy Lamarr](https://en.wikipedia.org/wiki/Hedy_Lamarr), [Ada Lovelace](https://en.wikipedia.org/wiki/Ada_Lovelace), [Alan Turing](https://en.wikipedia.org/wiki/Alan_Turing) and [Konrad Zuse](https://en.wikipedia.org/wiki/Konrad_Zuse). Very educational!

[IFA](http://b2b.ifa-berlin.com/) was happening at the same time. This added some security checks and we were surrounded by people in business suits. It was great that Droidcon ticket also gave us a chance to see new devices from various manufacturers, — I loved the Samsung exhibition just a few floors up. I welcome every chance I get to try out new Android devices!

![People using exercise bikes in front of big screens](/images/blogs/droidcon/samsung.jpeg)
*Samsung working on our Black Mirror future*

## Barcamp

My Barcamp highlights were SQLite panel, learning about hidden “features” of advertising libraries (careful, they might be doing more than you think!) and a session led by [@miphoni](https://twitter.com/miphoni) about taking over Android codebases. This made me think not only about how to best take over codebases, but also how to make my own code easy to understand, so anyone looking at it does not have to struggle. Also, the code you have written months ago is pretty much a new codebase when you look at it again, right? :) Our memory is pretty short and following defined standards, adding useful comments and refactoring hard classes helps not only with taking over the code, but with maintaining it for your future self.

Sadly, I have missed a session on sketchnoting from [@chiuki](https://twitter.com/chiuki), but it was definitely a big hit in the conference — too bad we can’t be in multiple rooms at once. Thankfully, there are plenty of resources online and I am learning this skill now after the conference. It was still useful to learn that it’s something I can look into.

![droidconGlobal wall](/images/blogs/droidcon/droidcon_global.jpeg)

## Day 1

Next day kicked off with keynote from [@chiuki](https://twitter.com/chiuki) — “How to be an Android Expert”. I want to be an expert! Turns out, it’s all about sharing knowledge. **Sharing gives you expertise.**

- Writing things down allows you to reconcile the knowledge you have and make connections you did not see before
- Everyone has something to share — ever struggled with anything and found a solution? Chances are, other people are struggling with the same thing as well.
- Sharing helps — and as developers we already want to solve problems. It’s an extension of that.
- Sharing does not have to be hard or high pressure — if you are just starting out, you have zero readers. This allows you to make mistakes and find your voice without judgement.
- You are helping your future self — chances are, you will forget about that solution you just found. Write it down and it’s there for you in a few months time.
- It’s ok to say you don’t know something. If you are afraid that you will be asked questions you do not know an answer to, “I don’t know” is perfectly reasonable reply.

We all can and should do this. I am starting with documenting my conference experience — look out for more blogs about Android from me in the future.

### Make your users happy

Two talks from day 1 about making a good impression — [Impress your user’s inner child!](http://droidcon.de/en/sessions/impress-your-users-inner-child) and [For optimists, our UI is pretty pessimistic](http://droidcon.de/en/sessions/optimists-our-ui-pretty-pessimistic). For me, these two talks resonated together.

![Photo shows a slide with two UI side by side: one with nice image and friendly text, the other plain and using unfriendly language](/images/blogs/droidcon/droidcon_global.jpeg)
*Which UI would you rather see?*

Empty screens are boring. Our UIs are also too pessimistic. We can improve this by adding animations to delight the user, rather than adding generic “no data here yet” message. We also need to spend more time thinking about loading and failure steps. This is something often missed out from designs, but it makes user experience so much better if we remember to consider these states.

### Design-developer cooperation

We had a great talk [How to bring a product to reality in a few days: design-dev cooperation and fast Android prototyping](http://droidcon.de/en/sessions/how-bring-product-reality-few-days-design-dev-cooperation-and-fast-android-prototyping) from a designer and a developer perspectives. Bad UX means the user makes mistakes — and that’s our fault. We can improve by always considering the needs of the user. If the change is important for UX and easy to implement, we should always prioritise it over difficult to implement and nice-to-have changes.

![Photo shows a graph with 4 sections for priority from easy to hard to implement to nice to have and important](/images/blogs/droidcon/priority_chart.jpeg)

### Code reviews

We already do code reviews, but any processes can be evolved further! These are some tips from the talk [Zen Code Reviews](http://droidcon.de/en/sessions/zen-code-reviews)

- If you make a pull request early and add to it gradually, other people in the team can have a look and start the discussion before it’s too hard to make many changes.
- Avoid back-and-forward — always finish entire code review, don’t stop at the first comment. This allows the developer to fix all issues at the same time.
- Leave useful comments. “This is terrible” — Bad. “This line might introduce a memory leak, you could use this method instead” — Good.

### Managing user feedback

Last talk of the day was [Managing User Feedback: How to Set Expectations and Translating Feedback into Features](http://droidcon.de/en/sessions/managing-user-feedback-how-set-expectations-and-translating-feedback-features). I think most important point to remember from this talk was — *You are **not your users**, no matter how technical your users are.*

![A chart showing computer skill level between 2011-2015](/images/blogs/droidcon/computer_skills_chart.jpeg)

The chart shows that only 5–8% of adults have strong technical skills and can overcome unexpected challenges — like unexpected pop-ups! This means that your users will likely struggle with things you find extremely obvious in your app. If anything is hidden behind multiple taps, chances are that users will not find it. Hamburger menu and pull-to-refresh is platform standard so you assume your users will know about it? It might be a wrong assumption to make.

You can create much better user interfaces by listening to your users and carrying out real-life tests. Statistics and surveys will not give you a full picture. Give your app to your non-technical friends and family members and see what problems they run into. The issues are not their fault — your app is probably not easy enough to use.

Remember to **listen to the users who come to you with problems**. It might be that an answer seems obvious to you, but not so much to your users. If someone is coming to you with a problem, most often they genuinely are trying to use your app and just need some help.

## Day 2

![Photo shows the speaker and the title slide of the keynote talk](/images/blogs/droidcon/keynote.jpeg)

Days 2 started with second keynote from [@ameellio](https://twitter.com/ameellio) [Designing for Trust: User Experience + Privacy](http://droidcon.de/en/sessions/keynote-designing-trust-user-experience-privacy). It made some interesting points about user trust and privacy. We are installing corporate surveillance equipment in our homes (that’s Alexa) and **selling our data for the cost of coffee** (loyalty apps requiring all the permissions). How do we protect our privacy? We can start by having consistent interfaces, making it easier for users to recognise whether the content they are looking at is legitimate, reinforce positive ideas (ie green lock is good), and coming up with easy-to-understand UX. For example, read receipts on WhatsApp are very easy to understand and change user behaviour.

### Offline first?

[Lessons from building Android apps for poor networks and low-end devices](http://droidcon.de/en/sessions/lessons-building-android-apps-poor-networks-and-low-end-devices) was a good reminder that network connectivity is still a very big issue. **Poor connectivity affects everyone** — even if you app does not target emerging markets, lost/poor connectivity easily becomes a problem just by entering an old building or being in temporary congested area (like a conference! though Wifi was working great throughout the conference in this case :) ). We all need to worry about bad networks, try to minimise network requests and consider whether we can have functionality when the app is offline.

### Lessons from distributed teams

The last talk I want to mention is from Realm — [The Good, The Bad and the Ugly — Building Distributed Teams at Realm](http://droidcon.de/en/sessions/good-bad-and-ugly-building-distributed-teams-realm). There are lessons to be learned here even if our company currently does not work across three time zones! :)

- Communication is very important —such as using slack efficiently, and making use of threads, so it’s easy to keep track of conversations.
- Try to unblock people where possible so everyone can carry on with their work without unnecessary delays
- Social interactions is important — have some fun slack channels and remember to do things as a team every so often

Most importantly, **assume the best in people**. It will help you work as a team and will reduce frustration.

![A photo of the quote on the slides](/images/blogs/droidcon/quote.jpeg)

>"Everyone did the best job they could, given what they knew at the time, their skills and abilities, the resources available, and the situation at hand
>
>-Retrospective Prime Directive"

*About building distributed teams, [@chrmelchior](https://twitter.com/chrmelchior) from [@realm](https://twitter.com/realm) [#droidconDE](https://twitter.com/hashtag/droidconDE?src=hash) — [@JerroTimo](https://twitter.com/jerrotimo)*

## Is it really over?…

The most important lesson of all repeated often throughout the conference: **it depends!** There are no black and white answers, you need to find a solution which works for your specific situation.

![Berlin at night from the plane window](/images/blogs/droidcon/berlin.jpeg)
Goodbye, Berlin!

Three days flew past. I have learned a lot and I am looking to applying things I learned. See you next year? :)

## Notes

This post has been previously published in [Medium](https://medium.com/@sigute/things-i-learned-at-droidconde-part-2-12898c1cffb).
