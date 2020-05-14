---
title: "Let go of your unused code"
date: 2018-03-23T00:00:00+01:00
---

![Phone, pen and a notebook titled "Creative Mess"](/images/blogs/unused_code/header.jpeg)

There are many parallels to be drawn between the software development and minimalism. I have noticed that the reasons unused code keeps hanging around the software projects are the same emotional reasons which cause clutter to collect at our homes. These are the reasons I have encountered most.

<!--more-->

## “Just In Case”

Everyone likes to feel prepared. Some preparation is good, like a few spare batteries in the kitchen drawer. Other times, we keep items only out of fear of needing them again, even if they long lost their value. That cable which doesn’t seem to connect to any appliance you own, but might be needed, anyone?

Same with code, you might have removed a feature, but what if this code block could be useful later? And so it stays in the codebase, getting stale, generating IDE warnings. Or maybe it’s commented it out, so it would actually take some effort to even get it to compile after re-adding.

Afraid to lose something important? Tag the commit in your source control and it will be there in the unlikely scenario where you need to bring something back.

## Emotional attachment

Some code is kept because it was hard to develop in the first place, and it would be a waste to discard something which took 3 weeks to write. Surely, it can be reused?

Maybe you did not even write it, the developer who started this project did, 5 years ago. If he/she did not remove it, then of course it must be important and will be needed any day now!

And graphic resources? You cannot lose these, they would absolutely work for some different feature, right?

Following the steps of [KonMari Method](https://konmari.com/about/the-method/), thank the code for the learning opportunity and then remove it from your project. If you developed it originally, that’s great, you have learned from it! If it’s so old that no one in the team remembers what it was for, it is past the time to let go.

## Resistance to change

The following is something I have heard a few times:

>“Sure, it’s not used at the moment, but it does not hurt by being there, why bother removing it? Just don’t look in that package”

But it does hurt! Especially when a new member joins the team and tries to understand the project. It’s extra mental load which can be removed easily.

## Not enough time

Now, sure, we all want to keep our codebase nice and tidy, but we have real work to do, there are always new features to add! Who even has time to go through and remove all this old stuff?

Imagine the world where adding new features is easy because your codebase is clean and nicely structured, and start moving towards that point by including cleanup in your work flow.

## Let it go…

Ask yourself why the old code is hanging around. Is it a rational reason?

**Make time to remove it and the rewards will be visible in no time!**

You will notice:

- Less logic to sift through when debugging.
- Easier to find relevant code.
- Improved build times.
- Easier maintenance — updating a library? Now you don’t have to update that section of code which is not even used.
- Easier on-boarding of new team members.

## Notes

Header photo by [Kaboompics.com](https://www.pexels.com/photo/top-view-of-phone-earphones-pen-and-diary-6662/).

This post has been previously published in [Medium](https://medium.com/@sigute/let-go-of-your-unused-code-e90cbd7148de).
