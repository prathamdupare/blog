---
author: "Pratham Dupare"
title: Material You for Linux with this GNOME extension 
date: 2022-08-05
description: You can get Material You theming for Linux"
tags: ["Linux", "Customization"]
thumbnail: "/material-you-linux.png"
---


## Material You for Linux
[Material You](https://material.io/blog/announcing-material-you) is wallpaper based theming introduced to Android 12 which themes the entire system by picking colors from wallpaper. If you like want Material You inspired personalization on Linux desktop, you just need one extension.

### Extension 
Enable [Material You Color Theming GNOME Extension](https://extensions.gnome.org/extension/5236/material-you-color-theming/). It can apply generated libadwaita theme from wallpaper using Material You.

Every time you change wallpaper, the extension generates a patched version of GNOME’s libadwaita theme with accent colors generated from wallpaper.

This can be applied to GTK3 apps using the [‘libadwaita’ GTK3 theme](https://www.omgubuntu.co.uk/2022/01/libadwaita-gtk3-theme), you can also color GTK4 Flatpak apps too once permission is granted through an app like [Flatseal](https://flathub.org/apps/details/com.github.tchx84.Flatseal). Instructions can be found on the [extension’s GitHub page](https://github.com/avanishsubbiah/material-you-theme).

The new theme is not applied automatically, you need to re-open the apps after generating the theme or even need to log in again. But, the results you get are worth the wait.

<img class="special-img-class" src="/material-you-linux2.png" />

Requirements:
You must be running GNOME 42, the extension is not supported by older versions. It will only work with libadwaita apps.

Extension update will reset all the changes made after disabled. If you want to revert to an older look, you can delete ~/.config/gtk-4.0/gtk.css and ~/.config/gtk-3.0/gtk.css .Remember to log in again for changes to take effect.

It is an impressive extension with a small size and can be accessed with the GNOME tweaks tool.

## See Also 
- [How to Switch To Linux - Step by Step Guide](/blog/switch_to_linux)
- [Reasons you need to use FOSS](/blog/fifthpost)


#### Comments

<script src="https://utteranc.es/client.js"
        repo="prathamdupare/fosspage_web"
        issue-term="pathname"
        label="Comment"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>