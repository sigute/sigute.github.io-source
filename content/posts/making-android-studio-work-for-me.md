---
title: "Making Android Studio work for me"
date: 2019-10-25T00:00:00+01:00
---

![Coloring materials, including paintbrushes, pencils and paint](/images/blogs/android_studio/header.jpeg)

When I install Android Studio, I like to make some adjustments which help me be more productive. These are my tips for customising Android Studio.

<!--more-->

## Theme and fonts

I prefer the dark theme for my IDE, I use [ChroMATERIAL](https://plugins.jetbrains.com/plugin/7998-chromaterial) Darcula. A dark theme might be helping with eye strain, though the research is inconclusive. I also find the default font too small and help my eyes by adjusting to at least 14pt, depending on the font. My current choice is Hack Nerd Font at 15pt.

> Preferences -> Editor -> Font -> Size

Cannot see enough lines of code with a bigger font? Make your methods shorter, reducing code complexity.

## Logcat Colours

By default, logcat shows everything in the same colour, making it hard to see a difference between a crash and a simple info log. I change the colours to help me see what is going on a bit easier, as well as making use of filtering features.
>Preferences -> Editor -> Color Scheme-> Android Logcat -> Untick “Use inherited values” and then choose your own colours.

![The picture shows Android Logcat colour scheme options](/images/blogs/android_studio/logcat.png)

## Code formatting

Unused imports, random spaces, inconsistencies between files... They can all be gone with code formatting. Even better, I [record a macro](https://android.jlelse.eu/android-studio-formatted-save-4db77c4c2396) to remove unused imports, reformat and save with one easy shortcut. I use `⌘ + S`.

Default formatting settings can be used or adjustments made to suit your needs. These can (and should) be shared with the entire team, and there will be no more disagreements about tabs or spaces in pull requests! (everyone knows which one is better 😉)

## Favourite plugins

I also use some plugins. I am not a heavy plugin user, but these are the ones I find pretty helpful.

**[Rainbow brackets](https://plugins.jetbrains.com/plugin/10080-rainbow-brackets/)** — makes matching brackets same colour, easier to quickly see what is going on. You can use the defaults, which are nice, or define a custom style.

> Preferences -> Editor -> Color Scheme-> Rainbow Brackers

**[Code Glance](https://plugins.jetbrains.com/plugin/7275-codeglance/)** — gives some additional context of where I am in the file, how long it is, etc. There are custom settings, but I stick with defaults.

**[Nyan Progress Bar](https://plugins.jetbrains.com/plugin/8575-nyan-progress-bar/)** — just a bit of fun! I spend enough time looking at the progress bar, at least now it is cute…

![Nyan car progress bar](/images/blogs/android_studio/nyan.png)

*Nyan car progress bar*

**[Nyan Tray](https://plugins.jetbrains.com/plugin/11286-nyan-tray/)** — adds another Nyan cat, and everyone would want more of these! But it also tells me how long gradle builds have been running in the last day/week/etc. If that number grows, it can indicate that it is time to look into strategies to reduce build times, or maybe upgrade the development machine...

As well as installing extra plugins, default preinstalled plugins can be disabled. For example, I work with git, so Mercurial and Subversion plugins are not useful to me. I did not notice a difference in performance after disabling them, but it reduced the number of options in the menus, which is still a win, as it helps me to focus on relevant content.

## Terminal

Not strictly Android Studio, but since I use both together every day, it deserves a mention. I use [iTerm2](https://www.iterm2.com/) with [Oh My Zsh](https://github.com/robbyrussell/oh-my-zsh) to make my terminal look and work better. I have used [these](https://medium.com/swlh/power-up-your-terminal-using-oh-my-zsh-iterm2-c5a03f73a9fb) [articles](https://hackernoon.com/how-to-trick-out-terminal-287c0e93fce0) to configure mine.

## Do you have a favourite setting?

How do you customise your Android Studio to work for you? Do you prefer all default settings? Let’s talk about it 😄

## Notes

Header photo: Colouring materials by [Sascha Düser](https://www.pexels.com/@sascha-duser-51514).

This post has been previously published in [Medium](https://medium.com/@sigute/making-android-studio-work-for-me-4aac9680e665).
