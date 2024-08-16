---
author: "Pratham Dupare"
title: My dev workflow - Linux, Hyprland ,Neovim and Tmux.
date: 2024-08-16
description: ""
tags: ["Reading"]
---

{{< alert >}}
Disclaimer: This is not a guide on how I rice my Window manager, what terminal I use, it's purely how I use my tools.
{{< /alert >}}

## Introduction

The time has come for me to share my developer workflow and how I use my tools to become a PRO developer!

### What I Don't Focus On

- GPU-rendered terminals (e.g., _Alacritty_).
- Ricing my desktop or color schemes.

### What Matters

- Speed
- Lower mental overhead

### The Tools I Use for the Perfect Developer Workflow

- **Linux** (of course!)
- **Window Manager**: Hyprland (with animations disabled)
- **Terminal**: foot (since I use Wayland)
- **Terminal Multiplexer**: Tmux

> **Note:** If you’re using Mac, great! Try to replicate this setup and find tools that make you fast and productive. If you use Windows, consider upgrading your RAM and playing some games; that's all I can suggest.

### Window Management

Most common Linux distros come with GNOME or KDE Plasma, which are excellent and a big reason for Linux’s recent improvements. However, I prefer not to use them because I don't want to rely on the mouse to manage windows. I prefer a window manager to streamline my workflow.

#### Tiling Window Manager

{{< figure
    src="/2024/developer/1.png"
    alt="Telescope"
    caption="Fuzzy finding file with Telescope"
    >}}

A tiling window manager automatically tiles and splits your windows, allowing you to quickly view and manage your open applications. I have set my `ALT` key as the main modifier, and use the following shortcuts:

- `Alt + 1` to switch to my browser on the 1st workspace.
- `Alt + 2` to switch to my terminal on the 2nd workspace.
- And so on, with workspaces typically maximized.

This setup allows me to quickly switch between tasks without worrying about window positions.

I can cycle through windows using `Alt + HJKL`, similar to Vim. Focused windows have highlighted borders, making navigation straightforward.

### Terminal Workflow

In my terminal, I use `tmux`, a terminal multiplexer that lets you split your terminal into multiple panes. This setup eliminates the need to switch between workspaces just to work on another terminal. It also helps me avoid multiple displays, which can be distracting and bad for posture.

#### Using Tmux

Tmux has a prefix key (`Ctrl + a` in my case) that triggers tmux commands. For example, after pressing the prefix key, you can switch between panes using numbers or navigate to the next pane with `prefix + n`. Tmux also keeps sessions alive, so if you accidentally close the terminal window, you can resume your work by running `tmux a`.

### Programming

{{< figure
    src="/2024/developer/0.9.png"
    alt="Telescope"
    caption="Fuzzy finding file with Telescope"
    >}}

For programming, I use Neovim instead of VS Code.

#### Why Neovim?

- VS Code is bloated and slow.
- Neovim runs in the terminal.
- I prefer Vim motions for efficient text editing.
- I don’t use the mouse (more on this later).

### Inside a Codebase

When starting work, I navigate to the desired directory and run `nvim .`, which opens Neovim in that directory (similar to VS Code’s `code .`).

#### Opening a File

{{< figure
    src="/2024/developer/2.png"
    alt="Telescope"
    caption="Fuzzy finding file with Telescope"
    >}}

I use Telescope, a fuzzy finder in Neovim, to search and navigate between files quickly. For example, to find `src/app/components/about/AboutUs.tsx`, I simply open Telescope by pressing `Space + Space` where space is the leader key and search for `about` in Telescope. It handles typos and finds the relevant file swiftly.

#### Moving Between Files

{{< figure
    src="/2024/developer/3.png"
    alt="Telescope"
    caption="Fuzzy finding file with Telescope"
    >}}

To manage multiple open files, I use the Harpoon plugin, developed by The Primeagen. Harpoon lets me mark frequently used files and switch between them easily without cluttering my workspace. It also saves cursor positions, enhancing productivity.

## Conclusion

This setup enables an exceptionally fast workflow and keeps development exciting. There is always room for improvement, and I’ve tailored my workflow to work best for me through experimentation and learning. The key is to try new things, step out of your comfort zone, and develop unique skills that make you a great developer.
