---
author: "Pratham Dupare"
title: Gaming on Linux — How To Play Any Game on Linux!
date: 2022-08-26
description: "Sometimes better than windows!"
tags: ["Productivity"]
thumbnail: "/2022/gaming-on-linux/gaming_on_linux.jpg"
---


Linux gaming is growing so popular.

The Steam deck has over 1.6 million users, and we expect them to grow more!

Unlike Windows, where you can play almost anything with a click, Linux gaming can be tricky. There are a lot of tools, software, and terms that can make things complicated.

This guide will cover everything including Steam, Epic Games, Ubisoft, and much more.

## Basic terms

**Proton**
Proton is a compatibility layer for Microsoft Windows games to run on Linux-based operating systems. It is a collection of software and libraries combined with a patched version of Wine to improve performance and compatibility with Windows games.

It creates a fake C Drive which games run on and then converts them to understand Linux inputs. It uses a lot of open-source libraries like Wine, DXVK, and VKD3D.

**Wine**
Wine is a compatibility layer capable of running Windows apps on Linux. It is not an emulator and can run apps natively and can be used to run games too!

**GE Proton**
It is a variant of the Proton and Compatibility tool for Steam Play based on Wine and additional components. It provides better compatibility and support but might not be as stable.

## Linux Distributions

<img class="special-img-class" src="/switch_to_linux/linux_distro.jpg" />

If you already use Linux you might know it doesn’t really matter which distro you choose, almost every distro comes with all the drivers pre-installed.

Pick any distro with the latest updates like Fedora, Ubuntu, Pop OS!, Arch, Manjaro, or anything you prefer.

**Drivers**
All the drivers required are already in the Linux Kernel, you don’t have to install them manually. When you update your kernel and distro, drivers get updated automatically. Intel and AMD provide their open-source drivers and are present in the kernel.

**Nvidia drivers**
Nvidia drivers are not open-source and hence are not added to the kernel. If you have an Nvidia GPU you will need to install Proprietary drivers. Just open your software store and search for “Nvidia” and install the latest version. It will support any GPU from Nvidia.

**Steam and Proton**
Steam is available for all distros and you can install it from your software center.

By default, Steam only lets you play games that have native support on Linux. But you can play other games too! To do that go to Steam Settings -> Steam Play and **Enable Steam Play for all other titles**. It uses Proton to run every windows game. But, it's not perfect, some games will run better with a specific version of Proton, some run better than others and maybe some games won’t even run.

You can check the compatibility, performance, and reviews on protondb.com. This website has a page for every game. It is categorized by labels.

**Platinum** — Native performance, no issues.

**Gold** — It means it runs really well but you might need to select a specific Proton version or do some tweaks.

**Silver** — Some things will not work like subtitles, audio, cutscenes, or glitches.

**Bronze** — The game will have issues and won’t provide good performance.

**Borked** — The game will not run.

You can look for comments and people with similar hardware to check compatibility and you will find all the necessary tweaks and arguments.

**Launch argument** can be added by going into game properties and pasting the argument in Launch Options.

**Proton Verison** can be changed in the Compatibility tab.

## Proton GE installation
Some versions might run better with Proton GE, to install it go to the proton-ge GitHub page and download tar.gz file from the releases page. Extract it and copy the contents inside.

Look for the **.steam folder** in the Home directory in the Steam folder, it is hidden so press **ctrl + H** to show hidden files. If it's not present, look for it in **.var/app/com.valvesoftware.Steam/.steam.** and create a new folder named **compatibilitytools.d** and open it. Paste the extracted files inside this folder.

After restarting Steam you'll find the Ge-Proton option in steam.

## Epic Games Store
The best solution for playing Epic games is using an unofficial client named **Heroic Games Launcher**. This lets you run games as you would with Steam Client.

<img class="special-img-class" src="/2022/gaming-on-linux/heroic_.png"/> 

You can also run games by using the official Epic Games Store client but you can't change the Proton Version for specific games meaning settings will apply to every single game.

Heroic lets you select tweaks and Proton versions for individual games. Install Heroic from your official Software store or from the Heroic website.

After installing, login to your Epic Games Store account. There are a tonne of options, you can change the install location, change the Proton version and also check the compatibility. It can also auto-detect your Steam’s installed Proton versions.

You can select a dedicated GPU if you have a hybrid graphics card like Nvidia.

## Ubisoft and Origin/ EA
These games are handled by Lutris.

**Lutris**
It is a game manager that can manage all of your Steam, Epic Games, Gog, Ubisoft, or EA games in one place.

Go to lutris.net/downloads and check the install instructions for your distribution. Click on the UBisobt or Origin icons and log in, then your games will be listed in the game window. Click to install the games you like.

Lutris shows you some scripts to choose from which are provided by users and install the best compatible version of proton or Wine. Choose the one you prefer and install the game.

**GoG**
For Gog, you can use Heroic game Launcher just like Epic Games. Other processes are similar and easy.

## What is FSR?
AMD’s FidelityFX SuperResolution (FSR) is a tool that you can use on any GPU. AMD’s FSR works by running the game in a lower resolution (thereby increasing performance), then using AI to upscale the image to your output resolution. AMD has recommended specific resolutions at which your game should run, depending on your screen resolution.

You can render a game at 720p and upscale it to your native resolution and the final output looks amazing! You can enable this setting in games that don't even support this.

FSR is only supported only by GE-Proton and not by the main Proton version.

**For Steam**
Add this argument: WINE_FULLSCREEN_FSR=1 %command% in Steam in the Game Properties -> Launch options tab.

**For Heroic Games Launcher**
Go to the game, then click on Settings and select GE-Proton in the Wine Version dropdown. Then check Enable FSR Hack below it.

**For Lutris**
Right-click on the game, select Configure, and go into Runner Options and **Enable AMD FidelityFX Super**.

## Conclusion
This is everything you need to start gaming on Linux, try playing your first game on Linux! Read the documentation, try different settings and enjoy! If you think this post provided you with some valuable information, give a clap and share.

Thank you!














#### Comments

<script src="https://utteranc.es/client.js"
        repo="prathamdupare/foss-page"
        issue-term="pathname"
        label="Comment"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>
