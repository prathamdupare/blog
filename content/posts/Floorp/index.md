---
author: "Pratham Dupare"
title: "Floorp - The Best Browser (For me)"
date: 2024-01-13
description: ""
tags: ["Android"]
thumbnail: "/featured.png"
---

## What is Floorp?

Floorp is essentially a fork of Firefox with added customizations and features. It's a free and open-source project with numerous contributors from Mozilla. You can explore the source code [here](https://github.com/Floorp-Projects/Floorp).

A special thanks to Chris Titus for introducing me to Floorp.

## Why not Firefox?

I love Firefox; it's excellent and the only true competitor for the Chromium-based browser monopoly. If the Floorp Project didn't exist, I would definitely go back to using Firefox.

## The Problem - VIM Navigation

As they say, "Once you learn Vim, there is no going back." I use Neovim as my primary IDE, and my Hyprland Window manager has Vim-like keybindings for selecting different windows. I wanted the same keyboard-centric navigation for my browser. Don't get me wrong; I don't hate using the mouse. I believe using both the mouse and keyboard together is optimal when needed, but some tasks can be performed faster with the keyboard.

I tried using an extension called [Vimium (Chrome)](https://chromewebstore.google.com/detail/vimium/dbepggeogbaibhgnhhndojpepiihcmeb?pli=1) or [Vimium-FF (Firefox)](https://addons.mozilla.org/en-US/firefox/addon/vimium-ff/). This is a fantastic extension that provides Vim-like navigation in your browser:

- **SHIFT+H** - Go back
- **SHIFT + (J, K)** - Move between tabs
- **O, SHIFT + O** - Search on the current/new tab

And much more.

However, for some tabs in Firefox or Chrome, you can't use these shortcuts.

## The Solution - Floorp

Floorp allows you to disable the built-in shortcuts and assign your own. This is perfect for my use case. Instead of relying on Vimium, I can use Floorp's built-in shortcuts!

Floorp also has other cool features, such as a double sidebar, the option to move the toolbar and tab bar anywhere, or vertical tabs built into it. I'm not a fan of these features; I prefer the default layout, but they are good to have.

## Finally..

While Floorp might me just another browser for someone, it's definitely the best one I have found.

## Installation

#### Linux

Install from PPA

    curl -fsSL https://ppa.ablaze.one/KEY.gpg | sudo gpg --dearmor -o /usr/share/keyrings/Floorp.gpg
    sudo curl -sS --compressed -o /etc/apt/sources.list.d/Floorp.list 'https://ppa.ablaze.one/Floorp.list'
    sudo apt update
    sudo apt install floorp

Install from Flathub

    flatpak install flathub one.ablaze.floorp
    flatpak run one.ablaze.floorp

Install from AUR with yay (For Arch Linux)

    yay -S floorp

#### MacOS and Windows

You can download .exe or .dmg from [Floorp's official website](https://floorp.app/en/download/)

## Finally...

While Floorp might be just another browser for some, it's undeniably the best one I have found.
