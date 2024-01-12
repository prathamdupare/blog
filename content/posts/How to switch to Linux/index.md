---
author: "Pratham Dupare"
title: How to Switch To Linux - Step by Step Guide
date: 2022-08-04
description: "Best Linux Distros to choose"
tags: ["Linux"]
thumbnail: "/switch_to_linux/switch_linuxl.png"
---
Switching to Linux is a great choice but at the same time, it can become scary. How to do it? What distro to choose? Will I need a new hard drive?

This guide will provide you with all the required steps.

So, if you are ready to use Linux, let's start!

## 1. Backup Your Data 

Backing up your data is a good practice, whether you want to switch to Linux or not, backup your data. It's easy, you just need to copy all the required files you might need and transfer them to an external hard drive  or cloud storage. 

Do not plug in your backup drive while doing this process.

## 2. Check the compatibility of your hardware

Linux is compatible with most anything these days still, you need to check if everything works. You can search online with the name of hardware and components. 

- **CPU and GPU** All drivers are available, Open drivers for Intel and AMD are available and proprietary drivers for Nvidia chips. Hard disks and SSDs won't be a problem. 
- **Wi-Fi and Bluetooth** -  You need to check the compatibility of Wi-Fi and Bluetooth components, search for your components, and you are done.

If you have other peripherals such as capture cards or gaming accessories, you should look them up as well, it will be easy.

## 3. Choose a Distro

<img class="special-img-class" src="/switch_to_linux/linux_distro.jpg" />

After you are done with the hardware, it's time to move to software. What is a Distro or Distribution? 

It is a Linux kernel with operating system tools that communicate with programs, a display server that allows windows, and menu bars to appear and then there is a desktop environment which is the interface you use and programs. 

Choosing a distro is the hardest part as there are so many choices, it depends on if you are a beginner or have tried them before or other preferences.

Most beginners will prefer [Ubuntu](https://medium.com/r/?url=https%3A%2F%2Fubuntu.com%2F) as it is simple and has a lot of documentation online, which will make your transition smooth. You can also try [Pop! OS](https://medium.com/r/?url=https%3A%2F%2Fpop.system76.com%2F). If you want customization you can pick [KDE Neon](https://medium.com/r/?url=https%3A%2F%2Fneon.kde.org%2F) which is highly customizable. If your computer has low resources, you can go for [Xfce](https://medium.com/r/?url=https%3A%2F%2Fwww.xfce.org%2F) or [Lubuntu](https://medium.com/r/?url=https%3A%2F%2Flubuntu.me%2F). 

If you are an advanced user, look for various distributions and pick the one which one works for you.

## 4. Create a bootable USB/ live USB

<img class="special-img-class" src="/switch_to_linux/etcher-1.png" />

Live USB is a live system of the distribution which runs on the USB and not your hard disk, it means every change you make will affect your USB and not your Hard disk. 

Once you choose a Distro, download the ISO file from the respective website. You will need a USB drive and software like [Etcher](https://medium.com/r/?url=https%3A%2F%2Fwww.balena.io%2Fetcher%2F) which will flash that file to your USB. You just need to select that ISO file and flash it.

Furthermore, you  can use this to check the compatibility of your hardware, and it won't change anything on your system. If you don't like it, you can change the distribution.

You will need to boot from the USB to check this, this process varies from system to system. Some boot directly when USB is plugged and for some systems, you need to make changes to your BIOS settings. You can go to the BIOS while starting the computer (Motherboard logo) by repeatedly pressing the function keys or the delete key (depends on your system).

Then look for boot sequence or priority under the boot section and set your USB to boot first. And save the changes, which will reboot.

## 5. Try your new Distribution
 Once you boot into the USB, you can experience your new OS/distro and explore it. Test everything you have - all peripherals, internet, browsers, Wi-Fi, camera, capture cards, and Bluetooth. If you like it, the next step is installation.

## 6. Install the Distribution

<img class="special-img-class" src="/switch_to_linux/ubuntu_usb_boot.png" />

ou can install the distro through the live USB and nowadays, they are super easy. Make sure you have backed up your data.

You will have two options:
- Wipe your drive and fresh installation which is easy.
- Dual boot with your existing operating system. This will make two partitions with two operating systems, and you will get the option to allot space. Look for instructions online.

<img class="special-img-class" src="/switch_to_linux/ubuntu_account.png" />

During installation, you will be asked to create a user  account, set a strong password and remember it because you'll need it multiple times while installing programs, changing configuration and for root access. 
After installation, the system will prompt you to reboot. If you dual boot, you will see an option to choose operating system, this is called GRUB (Boot Manager). This gives you the option to boot from older and newer kernels. If you face any issues with new kernel, just reboot and select older kernel7.

## 7. Explore the Linux Universe
Copy back your Backup data. Now you can try different things and software and learn few new things. Linux community is always ready to help you, check forums, play with it, install steam, some games, find documentation, ask questions and share your knowledge!

If you like Free and Open-Source software, check out our [FOSS Alternatives](https://medium.com/r/?url=https%3A%2F%2Ffosspage.com%2Fpage%2Falternative%2F).

Please visit [fosspage](https://medium.com/r/?url=https%3A%2F%2Ffosspage.com%2F) for more stuff like this!
 

#### Comments

<script src="https://utteranc.es/client.js"
        repo="prathamdupare/fosspage_web"
        issue-term="pathname"
        label="Comment"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>
