---
author: "Pratham Dupare"
title: Make Your Phone Perfect
date: 2023-01-20
description: "With 4 days of battery life!"
tags: ["Android"]
thumbnail: "/android_13.png"
---

# The Perfect Phone -

Your phone comes with a lot of stuff out of the box—a lot of features, but also a lot of unnecessary stuff. All of these distracting things can take away a lot of your precious time. Humans are not designed to constantly check their phones and have the thought of charging the phone every night in the back of their minds. This causes people to ignore real-life situations. 

But phones can do a lot—after all, they are computers in our pockets!

# The problem

- **Search**- Gone are the days when you would search dictionaries for the meaning of words. We have the Internet! But we rely on it to do everything, and that's bad.
- **Ongoing Notifications** It's like someone poking you every time they want attention.
- **Social Media** - You're aware.
- **Filling our leisure time** - When a person is not doing anything, he is by himself. That's absent in today's world: solitude.


# Solution
   
We need phones to do the only thing we need. It will give us time to think, increase battery life, and help you take control.


# We will only need two things:
- A pc with adb tools installed. You can see this quick guide by XDA [here](https://www.xda-developers.com/install-adb-windows-macos-linux/).
- USB debugging is enabled in developer options. If you don't have developer options, tap 7 times on build number **"About phone"** or **"Build Number"**.

# Install ADB on PC

**MacOS**

```js
brew install android-platform-tools

```

**Linux**

```js
sudo apt install android-sdk-platform-tools
```

**Windows**

- Download ADB Platform Tools
- Extract Tools to C:\Windows (This allows you to run adb.exe and fastboot.exe from anywhere.)
-  Install drivers for your phone - Install Android Device Drivers

## Check if it's working.

- Connect your phone to your PC.
- Open terminal or command prompt and type ``` adb devices```

- Your phone would be listed (accept the prompt on your Android device).


## Download Universal Android Debloater

Download the latest release from https://github.com/0x192/universal-android-debloater/releases

Launch it.


<img class="special-img-class" src="/2022/perfect-phone/uad.png"/> 

## Time to Debloat

After connecting your phone to your PC, I would suggest removing all recommended packages. You can add the required Google-related stuff afterwards.

Note that this will remove basic apps such as Calculator, Calendar, Photos, etc. Simply uncheck the tick boxes if you don't want them removed.

## Change your Launcher

You can choose any Launcher you want, I prefer [Niagara Launcher](https://play.google.com/store/apps/details?id=bitpit.launcher&hl=en_US&gl=US) or [Lawnchair](https://github.com/LawnchairLauncher/lawnchair/releases/tag/1.2.0.1884).
The launcher that comes with your device has a lot of dependencies that slow the phone down and sap its power.

Set the required apps to your homescreen, and you're done!

This is what my phone looks like.

<img class="special-img-class" src="/2022/perfect-phone/niagara_launcher.png" style="height: 585px; width:270px;"/>





























































































