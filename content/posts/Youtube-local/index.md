---
author: "Pratham Dupare"
title: Youtube Local
date: 2023-04-04
description: "youtube-local is a browser-based client written in Python for watching Youtube anonymously"
tags: ["Linux"]
thumbnail: "/android_13.png"
---

If you are searching for a youtube frontent that is bloat-free and follows the principle of doing the basic thing and doing it the best then youtube-local is the best option.

I will tell you what is yt-local and how I set it up.

## What is yt-local?

youtube-local is a browser-based client written in Python for watching Youtube anonymously and without the lag of the slow page used by Youtube. One of the primary features is that all requests are routed through Tor, except for the video file at googlevideo.com. This is analogous to what HookTube (defunct) and Invidious do, except that you do not have to trust a third-party to respect your privacy. The assumption here is that Google won't put the effort in to incorporate the video file requests into their tracking, as it's not worth pursuing the incredibly small number of users who care about privacy (Tor video routing is also provided as an option). Tor has high latency, so this will not be as fast network-wise as regular Youtube. However, using Tor is optional; when not routing through Tor, video pages may load faster than they do with Youtube's page depending on your browser.

This is litrally what's written on its github page.


## Features

* Standard pages of Youtube: search, channels, playlists
* Anonymity from Google's tracking by routing requests through Tor
* Local playlists: These solve the two problems with creating playlists on Youtube: (1) they're datamined and (2) videos frequently get deleted by Youtube and lost from the playlist, making it very difficult to find a reupload as the title of the deleted video is not displayed.
* Themes: Light, Gray, and Dark
* Subtitles
* Easily download videos or their audio
* No ads
* View comments
* Javascript not required
* Theater and non-theater mode
* Subscriptions that are independent from Youtube
  * Can import subscriptions from Youtube
  * Works by checking channels individually
  * Can be set to automatically check channels.
  * For efficiency of requests, frequency of checking is based on how quickly channel posts videos
  * Can mute channels, so as to have a way to "soft" unsubscribe. Muted channels won't be checked automatically or when using the "Check all" button. Videos from these channels will be hidden.
  * Can tag subscriptions to organize them or check specific tags
* Fast page
  * No distracting/slow layout rearrangement
  * No lazy-loading of comments; they are ready instantly.
* Settings allow fine-tuned control over when/how comments or related videos are shown:
  1. Shown by default, with click to hide
  2. Hidden by default, with click to show
  3. Never shown
* Optionally skip sponsored segments using [SponsorBlock](https://github.com/ajayyy/SponsorBlock)'s API
* Custom video speeds
* Video transcript
* Supports all available video qualities: 144p through 2160p



## My Setup

First, I made a folder in my $HOME directory(I use Arch btw!) and cloned the Git-Hub repo into it.

cd into that folder and you just have to run the **server.py** file in the terminal and it will start the server at **http://localhost:(something)**. In my case its  **http://localhost:8080**.

When you visit the server, you will get a simple minimal GUI. But you don't want to run **server.py** everytime you start your computer.

I made a simple bash script:

```
#!/bin/bash
cd /home/pratham/yt-local/
python3 server.py

```

I use Hyprland so I saved it as ytlocal in hyprland's scripts folder.
If you are using some desktop enviornment, add the command in your startup from settings.

And then added few lines to my startup file.

```
#!/bin/bash

SCRIPTSDIR=$HOME/.config/hypr/scripts

# Launch yt-local
${SCRIPTSDIR}/ytlocal &


```
Now whenever you start your PC the script will run automatically in the background. You just have to visit localhost.

You can also redirect your site whenever you search youtube.com to localhost by using extensions like Redirector.

Enjoy you privacy and minimalism!
















