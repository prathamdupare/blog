---
author: "Pratham Dupare"
title: "Vulkan Beta Driver 515.49.10 released for Linux"
date: 2022-07-21
description: ""
tags: ["Linux"]
thumbnail:  "/vulcan_515.png"
---

NVIDIA released a upgrade to their new developer-focused version 515.49.10. [Vulkan Beta Drivers](https://developer.nvidia.com/vulkan-driver).

**July 20th, 2022 - Windows 516.89, Linux 515.49.10**

Changes: 

- New:
[VK_EXT_pipeline_robustness](https://registry.khronos.org/vulkan/specs/1.3-extensions/man/html/VK_EXT_pipeline_robustness.html)

- Fixes:
    - Restored old shader disk cache behavior to remain enabled even if the app uses its own pipeline cache
    - Fixed issue with optimized graphics pipeline library final link using the wrong shaders
    - Fixed issue with some fp16 shader operations
- open-gpu-kernel-modules release:
    - https://github.com/NVIDIA/open-gpu-kernel-modules/releases/tag/515.49.10

These drivers are for developer use only and you should prefer stable releases.

The newest stable versions of the main NVIDIA driver for Linux are NVIDIA 515.57 released on June 28, 2022 from their "Production Branch" series or 495.46 released on December 13, 2021 from their "New Feature" series. Both Production and New Feature series are fine for normal use.

#### Comments

<script src="https://utteranc.es/client.js"
        repo="prathamdupare/fosspage_web"
        issue-term="pathname"
        label="Comment"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>