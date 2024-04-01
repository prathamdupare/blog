---
author: "Pratham Dupare"
title: Minimal notetaking with Neovim and Obsidian.
date: 2024-04-01
description: "Obsidian and Neovim"
tags: ["Android"]
thumbnail: ""
---

## WHY?

Several years ago, I experimented with Obsidian for a while, finding it useful initially. However, as an advocate for free and open-source software, I discovered that Obsidian wasn't open-source, prompting me to abandon it.

### Present Situation

By 2024, I found Neovim to be immensely satisfying, although not for note-taking purposes. My needs were simple - I required a platform to jot down daily tasks, links, or to-dos, without any frills. While I attempted to use Neovim for this, the challenge arose when I wasn't always near my laptop. Hence, I sought a solution to synchronize my notes with my phone. My initial thought was to sync them using Syncthing (which I'll discuss further). However, I still needed to access the notes through a text editor on my phone, which wasn't ideal.

## Solution

## WHY?

Many years ago I tried using Obsidian , for some time I did it too. But then as a free and open source enthusiast I came to know that Obsidian was not open-source which made me leave it.

### Now

In 2024, I was more than satisfied with Neovim, but notetaking was not my thing. I just needed something where I could jot down something like daily tasks or links or some to-do, nothing fancy.

Many times I tried using Neovim for this but the problem was that not everytime I was around my laptop. So I needed a way to sync my notes to my phone. I thought of syncing them with Syncthing (which I will talk about later). But I still had to open the files app on my phone, to see the notes in some random text editor.

## Solution

One day, I saw `TJ DeVries` on Youtube using Obsidian for notetaking. I was like how could a core maintainer of Neovim use Obsidian, then I researched and got to know that Obsidian had a vim mode too, I was soo happy to see that! But it didnt solve my problem,

There were two probems:

1. Even if Obsidian had vim mode, I would forget to open the app. I was not programmed to do it.
2. Even with vim mode, I still had to use mouse to switch between the notes, I think Obsidian has shortcuts, but it was whole another thing to learn just for notetaking.

Then I remembered that I could also edit the Notes within the folder where Obsidian vault is situated, and that made things so much easier!

## The Setup

### Laptop

I have Obsidian installed just to make the vault/folder in my Home directory. I just Vim into it and change whatever I want and Syncthing takes care of everything else.

### Syncthing

#### What is Syncthing

Syncthing is a continuous file synchronization program. It synchronizes files between two or more computers in real time, safely protected from prying eyes. Your data is your data alone and you deserve to choose where it is stored, whether it is shared with some third party, and how it’s transmitted over the internet.

I installed syncthing on both Laptop and Android and Linked my Obsidian folder. You can see the tutorial by [Mental Outlaw](https://www.youtube.com/watch?v=Uag8PJaO0N4) or [DistroTube](https://www.youtube.com/watch?v=i6LuV7Pl2YU).

This would sync my folder realtime when both devices were on!

### Android

I installed Obsidian and Syncthing and select the already created/synced folder from syncthing!

Now I could view the notes and edit them wherever I wanted and it would almost instantly reflect on my desktop too!

Also, this design is essentially makes two backups on your devices!
I could also make a git repo and wrote a scripy to run a cron job to automatically backup them on GitHub but Microsoft should not own everthing right?!

## Conclusion

No conclusion, I will keep using this setup I dont know for how long maybe forever or use something completely different who knows!
One day, I stumbled upon a YouTube video featuring TJ DeVries using Obsidian for note-taking. I was intrigued - how could a core Neovim maintainer use Obsidian? Upon researching, I discovered that Obsidian offered a Vim mode, which delighted me. However, this didn't fully address my issues:

1. Even with Obsidian's Vim mode, I often forgot to open the app.
2. Despite the Vim mode, I still had to resort to using the mouse to navigate between notes. While Obsidian provided shortcuts, it felt cumbersome to learn them solely for note-taking purposes.

Then it struck me - I could edit the notes directly within the folder where the Obsidian vault was located, simplifying the process significantly!

## The Setup

### Laptop

I installed Obsidian solely to create the vault/folder in my home directory. I would then use Vim to access it and make any necessary changes, while Syncthing handled the synchronization in the background.

### Syncthing

#### What is Syncthing?

Syncthing is a continuous file synchronization program that securely synchronizes files between two or more computers in real-time. Your data remains private, allowing you to choose where it's stored and whether it's shared with third parties.

I installed Syncthing on both my laptop and Android device, linking it to my Obsidian folder. You can find tutorials on how to do this by watching videos from creators like [Mental Outlaw](https://www.youtube.com/watch?v=Uag8PJaO0N4) or [DistroTube](https://www.youtube.com/watch?v=i6LuV7Pl2YU).

This setup ensured that my folder was synced in real-time whenever both devices were online!

### Android

On my Android device, I installed Obsidian and Syncthing, selecting the previously created/synced folder from Syncthing.

Now, I could view and edit my notes wherever I wanted, with changes almost instantly reflected on my desktop too!

Moreover, this setup essentially provided two backups of my notes on separate devices!

I also considered creating a Git repository and writing a script to run a cron job for automatic backups on GitHub. After all, shouldn't Microsoft monopolize everything, right?!

## Conclusion

There's no conclusion - I'll continue using this setup indefinitely, or until I decide to explore something entirely different. Who knows what the future holds!
