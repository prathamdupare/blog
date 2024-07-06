---
author: Pratham Dupare
title: Test Schema
date: 2022-07-25
description:
keywords: ["alternative", "FOSS", "contact"]
type: alternative
---



### This is basic representation of how our project structure might look like.
```
my-nextjs-app/
├── app/
│   ├── about-us/
│   │   ├── page.tsx
│   ├── contact/
│   │   ├── page.tsx
│   ├── home/
│   │   ├── page.tsx
│   ├── products/
│   │   ├── [id]/
│   │   │   ├── page.tsx
│   ├── services/
│   │   ├── page.tsx
│   ├── layout.tsx
│   ├── globals.css
├── components/
│   ├── Header.tsx
│   ├── Footer.tsx
│   ├── MyContainer.tsx
│   ├── Notification.tsx
│   ├── portfolio-builder/
│   │   ├── Education.tsx
│   │   ├── Experience.tsx
│   │   ├── Footer.tsx
│   │   ├── Header.tsx
│   │   ├── PortfolioView.tsx
│   │   ├── Profile.tsx
│   │   ├── Projects.tsx
│   │   └── Skills.tsx
├── providers/
│   ├── ThemeProvider.tsx
│   ├── NotificationProvider.tsx
├── utils/
│   ├── index.ts
│   ├── zod/
│   │   ├── schema1.ts
│   │   ├── schema2.ts
│   │   └── ...
│   ├── helpers/
│   │   ├── util1.ts
│   │   ├── util2.ts
│   │   └── ...
│   ├── actions/
│   │   ├── action1.ts
│   │   ├── action2.ts
│   │   └── ...
├── next.config.js
├── tsconfig.json
├── package.json
├── README.md
```

## File and Folder Naming Conventions


In NextJS, it is recommended to use lowercase letters and hyphens to separate words in file and folder names. This makes it easier to read and avoids confusion when working with different file types. For example, instead of using AboutUs.js, use about-us.js.


## Component Naming Conventions

When creating components, it is best to use PascalCase for naming. This convention makes it easier to differentiate between components and regular HTML elements. For example, instead of using my-container, use MyContainer.

## Route Naming Conventions

Routes in NextJS should follow the same naming conventions as file and folder names. This makes it easier to identify routes and avoids confusion when navigating through your application. For example, instead of using /aboutUs, use /about-us.

## utils

We will keep all the utils in the same file, no "lib" directory.
This will avoid confusion about where to put the supporting files.

This will also contain zod, helpers and actions.

## Providers 
Providers will go to the Providers folder, like theme-providers, notification-provider in root of the project.



