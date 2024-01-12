---
author: "Pratham Dupare"
title: Make Ubuntu avoid entering suspended mode when the laptop lid is closed.
date: 2022-09-07
description: "Two methods"
tags: ["Productivity"]
thumbnail: "/2022/ubuntu-lid-suspend/ubuntu-lid-suspend.jpg"
---
Our laptops suspend when the lid is closed, it is the default behavior of any laptop. It is a good feature that helps to save battery but if you are using a laptop as a server that needs to run constantly then it can cause problems. 

If you are using Ubuntu then you can turn that off.

## Method 1 :


This is the simplest method and doesn't require any command line and works with any Distro with a GNOME desktop.
If you use the GNOME desktop, you might use Gnome Tweaks for various reasons.
You can install the GNOME tweaks tool from the software center.

Or run the following command:
```
sudo apt install gnome-tweaks
```

<img class="special-img-class" src="/2022/ubuntu-lid-suspend/gnome-tweaks-suspend.png"/> 

After installing the app, open it. In the "General" tab toggle off "Suspend when the laptop lid is closed". 
That's all, just restart your system for changes to take effect.

## Method 2 :
This method requires you to change login configuration (recommended for advanced users)

### For Ubuntu :
Open **/etc/systemd/logind.conf**. 
Or run the following command in the terminal:

```
sudo gedit /etc/systemd/logind.conf
```

### For Ubuntu server without UI :
use **nano** text editor instead

You will find three lines of default settings for the laptop lid closing.

- HandleLidSwitch: When the laptop is on battery power
- HandleLidSwitchExternalPower: When the laptop is plugged into a power outlet
- HandleLidSwitchDocked: When the laptop is connected to a docking station

<img class="special-img-class" src="/2022/ubuntu-lid-suspend/lid-commands.png"/> 


The laptop will suspend irrespective of whether it is connected to power or not.

 According to your preference, you can change the value to:

- lock: lock when the lid is closed
- ignore: do nothing
- poweroff: shutdown
- hibernate: hibernate when the lid is closed

Either create a new file in the **/etc/systemd/logind.conf.d** directory or edit the **/etc/systemd/logind.conf** file, uncomment the written settings, and alter their value. If it doesn't already exist, create it.

If you know the command line use method 2 otherwise use GUI **Method 1**.

Try these methods and let me know if you have questions. 

Hope this helps.


#### Comments

<script src="https://utteranc.es/client.js"
        repo="prathamdupare/foss-page"
        issue-term="pathname"
        label="Comment"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>
