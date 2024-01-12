---
author: "Pratham Dupare"
title: Consume Internet The Better Way
date: 2023-02-13
description: "Consume internet the better way"
tags: ["Android"]
thumbnail: "/android_13.png"
---

## 1. Newsboat

<img class="special-img-class" src="/2023/newsboat/newsboat.png"/>

### History of RSS

RSS stands for (Really Simple Syndication). It is used to distribute frequently updated content on a website. It is an old tool which was developed in 1990s.The goal was to help people receive updates from multiple sites, just like you subscribe to your favorite YouTube channel. With RSS you can get updates from your favorite websites like [fosspage.com](fosspage.com).

RSS feeds were really popular in 2000s, overtime their popularity decreased, with the emergence of social media and other sites that pulls you in a rabbit hole.Still this is a perfect tool for people who want to prioritize work and want to stay away from distractions.

Newsboat is a simple terminal based RSS Feed reader which works on Linux. It is active maintained. You can check the GitHub repo [here](https://github.com/newsboat/newsboat).

You can easily install newsboat from your distribution's repository [(a lot of distros have a package)](https://repology.org/project/newsboat).

#### Features

Among the features that stand out of Newsboat, we can find:

- Supports RSS 0.9x, 1.0, 2.0 and Atom
- Keyboard control with the ability to define your own key combinations(Yes you can configure VIM keybindings!!)
- Find all uploaded feeds
- Classify your subscriptions using tag system
- Change colors and customize
- Import and export of OPML subscriptions
- Ability to sync feeds with Google Reader.

#### Install via snap:

```
sudo snap install newsboat
```

#### On Arch Linux using yay

```
yay -S newsboat
```

or

```
sudo pacman -S newsboat
```

#### Or you can clone and install

```
git clone git://github.com/newsboat/newsboat.git
```

And then run:

```
make
sudo make install
```

### Configuring or adding feeds

<img class="special-img-class" src="/2023/newsboat/url.png"/>
Now you have installed newsboat, but first we need to configure and add urls.

You will find **.newsboat** folder in your home directory. If it doesn't, exist create a folder with the same name written here.

Under this folder create a file named **"urls"**.

Paste all the RSS links you need into this file. You can use any text editor to edit these files. I prefer Vim.

This website also has a RSS feed, you can paste this link inside urls file:

```
https://fosspage.com/index.xml
```

Finding RSS links for sites can be frustrating. Luckily, There are a lot of extensions that make it easy to find them.

I use [Awesome RSS](https://addons.mozilla.org/en-US/firefox/addon/awesome-rss/) which is a Firefox extension.

For Chromium browsers like Chrome and Brave, you can use [RSS Feed Reader](https://chrome.google.com/webstore/detail/rss-feed-reader/pnjaodmkngahhkoihejjehlcdlnohgmp?hl=en).

Once you visit a site you will see RSS icon above, click on that icon, copy the link and paste it into your **urls** file.

Your browser might render the xml url, but we just need that url, copy it from url bar.

### Bonus

You can subscribe to YouTube channels too! Awesome RSS or any extension will find them for you. There is another way to get them through source code but we won't get into that. Looks like YouTube and Google don't want to share their RSS links!

Finally run into your terminal:

```
newsboat
```

You will be greeted with a minimal but beautiful list of websites. Navigate with arrow keys and press Enter to select a website. Newsboat will refresh last 15 posts.

You are done!

### Optional Customization

Newsboat can be configured in any way you want, it can also open the feeds in browser, play YouTube directly in MPV or VLC player and much more!

You can use my [newsboat configuration](). Simply paste the config file in **.newsboat** folder.

This will enable:

- Vim keybindings
- Beautiful Color scheme and highlights
- Set **(, + V)** to open playable video links in MPV
- Set **(, + F)** to open posts in Browser

Of course, you can customize it to your liking, just go through the [Documentation](https://newsboat.org/releases/2.18/docs/newsboat.html).

## 2. Youtube via Terminal

<img class="special-img-class" src="/2023/newsboat/youtube_terminal.png"/>

What if I told you you can watch YouTube videos right from the comfort of your terminal. Okay, newsboat can do that but what if you need to search something on youtube and play it.

I am going to show you a elite way to do that.

Go to this [GitHub repo](https://github.com/sayan01/scripts/blob/master/yt)

1. Click on Raw and copy the script.
2. Go to your home directory and create a file named yt.sh
   or run this command in your terminal.

```
touch yt.sh
```

3. Open the file and paste the copied script into this file.

4. Go to Home Directory and open a file named **.bashrc** and add the following line to it:

```
alias yt='./yt.sh'
```

5. Run "yt" inside terminal and you should see search box. Search the term you want and you will see results. Navigate with arrow keys and select the video you want to play.

Note that this script does not use YouTube API and hence can't display thumbnails.
