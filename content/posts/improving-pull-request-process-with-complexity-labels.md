---
title: "Improving Pull Request Process with Complexity Labels"
date: 2020-03-12T00:00:00+01:00
---

![Sticky notes and pens](/images/blogs/pull_request_labels/header.jpeg)

Does your team struggle with pull requests? Is there never enough time in the day to review others code? Do you feel like you need to keep asking your teammates for code reviews? Is the list growing everyday with no end in sight? Pull requests **are** hard. Our Android team at Microsoft To Do made some changes recently to improve the process. I have suggested adding labels to pull requests and this article shows my solution.

<!--more-->

## What is complexity

To start with, I thought about how we define complexity. Take a moment to consider these: What makes a pull request easier or harder to review? Is there a type of pull request which always get merged straight away and another one that sits there for a long time? What's the difference between them?

In general, the smaller the pull request, the easier and faster it should be to review. This is a good general rule, however one line change is not always straight forward in terms of impact. Fixing a typo is easy. Updating an external dependency also changes only a few characters, but might lead to the entire app breaking.

However, considering only the number of lines of code changing can be misleading if it is the only way to think about complexity. On the other side of this, large pull requests are not necessarily complex. Renaming something might affect hundreds of files but the risk is low, especially with modern tools where forgetting some files is less likely. Adding in new translations could also generate very large changeset, but is unlikely to generate new bugs.

## Complexity Matrix

After considering size and difficulty, I have arrived at complexity as the measure of pull request.

**Size x Difficulty = Complexity**

I have created this matrix as a way to think about complexity and roughly estimate where pull request might fall into.

![A table showing size and difficulty with 4 corners highlighted, summarised further below](/images/blogs/pull_request_labels/complexity_matrix.jpeg)

### Easy - small size and low difficulty

These are your small and simple pull requests. This is the quickest pull request type to review and the easiest to test. Changes are unlikely to cause further issues. These pull requests tend to get merged very quickly.

### Medium Low - large size and low difficulty

These are pull requests which are large, but the changes themselves are trivial. They can take longer to review because of the size, but are also less likely to introduce further bugs.

Where possible, it could be beneficial to split these pull requests into multiple smaller ones.

### Medium High - small size and hard difficulty

These are pull requests which do not change many lines of code, but could have a big impact. This includes changing business logic, UI elements, updating dependencies, etc. These changes can potentially have unforeseen effects, so need to be reviewed and tested carefully.

This is the category where using strategies like A/B testing, feature flags and and staged releases could be very beneficial, so changes can be reverted easily in case of any issues, whether with code or with user impact (for example if new UI does not perform as well as expected).

### Large - large size and hard difficulty

The final category is the pull requests which are large and complex. This could be things like adding a new screen to the app, changing one dependency to another, refactoring, etc. The bigger a pull request grows in this area, the harder it is to keep track of changes and carry out a good code review.

The best strategy here is to be careful about creating pull requests in this category. If the code changes are growing, could they be split across multiple code reviews? For example, for a new app feature, database changes could be reviewed separately from the UI layer. Using feature flags to hide code which is not ready for production yet helps with this, so the feature branch does not grow too much out of sync with the main branch.

## How to put this into practise

We have started labelling our pull requests as part of the title and use t-shirt sizes as the complexity:

> S -> M -> L -> XL -> ... -> XXXXXXL?

Some examples of pull request titles would look like this:

> [S] Fixed accessibility bug in X screen
>
> [M] Updated library Y dependency, please test

Alternative labels could include emojis!

> 🐇 -> 🦘 -> 🦙 -> 🦖
>
> 😀 -> 🙂 -> 😐 -> 😭

Be aware that emojis appear differently on other devices, dependent on platform, OS, and many other factors, so make sure the selected ones look good on all your teammates computers!

If you want to use animal emojis, I have categorised some of them by size!

<!-- https://twitter.com/Sigute_K/status/1234832806544625665 -->
{{< tweet 1234832806544625665 >}}

As well as using the label as part of the title, you could make use of labels in your code review tools.

If you are using Github, you can create custom labels and then add them to pull requests. Emojis and colours are supported and you will be able to filter by specific label.

![Screenshot of Github pull requests with custom complexity labels](/images/blogs/pull_request_labels/example_github.png)

## Impact of changes

It has been a few weeks since our team started adding a complexity label when making new pull requests. In general, the feedback has been great! This approach encourages us to think about how complex the changes are when we add new code to Android Microsoft To Do app.

The benefits of this approach so far include:

- Telling at glance how much time it might take to review the changes. This helps to plan which pull requests might need a longer time to review and what can be quickly reviewed in the spare 10 minutes between other tasks.
- Thinking about complexity when creating pull requests and strategies to mitigate risk.
- The pull request list becomes more manageable.

We did not experience any big issues, but a few things we discovered:

- It is hard to get used to any new approach, so remembering to add a label is not automatic yet.
- Our release notes made use of pull request titles for the draft version, so we had to add an additional script to strip the labels out as part of our continuous integration process.

As a closing thought, I would encourage you to be forgiving about the labels. They are rough indicators intended to help with the process. If you are getting lost in conversations over whether a pull request is XL or XXL, you are missing the point! 😀

## Notes

Header image: Sticky notes and pens by [Maria Tyutina](https://www.pexels.com/photo/white-click-pens-1017502/)

This post has been previously published in [Medium](https://medium.com/@sigute/improving-pull-request-process-with-complexity-labels-e47a59c54f21) and [dev.to](https://dev.to/sigute/improving-pull-request-process-with-complexity-labels-5bgf).
