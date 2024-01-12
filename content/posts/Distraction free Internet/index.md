---
author: "Pratham Dupare"
title: Distraction free Setup
date: 2023-11-07
description: "..."
tags: ["Android"]
thumbnail: "/featured.png"
---

# Distractions

In today's digital age, it often feels like everyone on the internet is thirsty for your attention. Whether you're browsing through your favorite websites, scrolling through social media, or even just checking your email, it seems like every online platform is equipped with an arsenal of tools designed to keep you engaged for as long as possible. While these platforms are undoubtedly convenient and entertaining, they can also be a significant source of distraction and time-wasting.

If you're truly willing to take your productivity to the next level, it's essential to address these attention-draining leaks in your online routine. On your computer, these leaks typically manifest in the form of your web browser, the specific websites you frequent, and the content you consume. To regain control over your online activities and channel your time and energy more effectively, it's crucial to identify and seal off these leaks.

## The Setup

1. Install [uBlock Origin](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm): This top-notch ad blocker not only banishes annoying ads but also works its magic on YouTube, giving you an ad-free viewing experience.

2. Set Brave as Your Default Search: Make Brave your go-to search engine for a more privacy-focused browsing experience. You can still use it to search on Google if needed.

3. Install [Unhook](https://chrome.google.com/webstore/detail/unhook-remove-youtube-rec/khncfooichmfjbepaaaebmommgaepoid): Say goodbye to distracting YouTube features with Unhook, which helps you regain control over your video-watching experience.

4. Add [Redirector Extension](https://chrome.google.com/webstore/detail/redirector/ocgpenflpmgnfapjedencafcfakcekcd): This handy extension allows you to customize and redirect web pages, helping you tailor your online interactions to your preferences.

I use RSS feeds to get info from the internet. You can see my previous setup [here](https://fosspage.com/posts/consume-web-in-a-better-way/).

Now, I use [Fresh RSS](https://freshrss.org/index.html), FreshRSS is a self-hosted RSS and Atom feed aggregator. It is lightweight, easy to work with, powerful, and customizable. You can see the installation methods [here](https://github.com/FreshRSS/FreshRSS/tree/edge), I won't explain it here.

I used Docker Compose to set it up and run it on port 8585.

After installing it, go to `localhost:[the port that you have set up]` – for me, it's 8585.
When you visit it, you will see the Fresh RSS page.

You can use Fresh RSS to aggregate all RSS feeds, news feeds, and even your favorite YouTube channels. There is even a plugin that lets you watch YouTube inside Fresh RSS!

Now, we are almost done. You might be thinking, why would you go to `localhost:8585` every time you open your browser? That's where Redirector comes in. The idea is simple: whenever you type "youtube" in your browser, it should redirect you to Fresh RSS!

## Redirector Setup

Once you install Redirector, click on the browser's toolbar to open Redirector and click on "Edit Redirects."

- Click on "Create new redirect."
- In the description, add "Youtube."
- In "Example URL," enter `https://www.youtube.com`.
- Include pattern: `youtube.com`
- Redirect to: `http://localhost:8585`
- Set pattern type to "Regular Expression."
- Pattern Description: `^https?://(www\.)?youtube\.com/?$`
- Click "Show advanced options."
- Set Exclude pattern: `^https?://(www\.)?youtube\.com/[^/].\*$`

And then hit save.

Now, every time you visit `youtube.com`, you will get redirected to Fresh RSS!

But what if you want to search YouTube for something? That's where Brave Search comes in. With Brave Search, you can use !bangs to search directly from the browser's search bar.

- If you want to search "hello world on Google," you will search "hello world !g."
- Similarly, for YouTube, "hello world !yt." This time it won't redirect to Fresh RSS because we set that Exclude pattern.

Finally, go to Unhook from the toolbar and turn on everything that you want to remove from YouTube.

There you go, that's your setup for a distraction-free internet.
