---
author: Pratham Dupare
title: Test Schema
date: 2022-07-25
description:
keywords: ["alternative", "FOSS", "contact"]
type: alternative
---
```
our-next-app/
├── app/
│   ├── (auth)/
│   │   ├── api/
│   │   │   └── [...]
│   ├── (root)/
│   │   ├── home/
│   │   │   └── page.tsx
│   │   ├── about/
│   │   │   └── page.tsx
│   │   ├── contact/
│   │   │   └── page.tsx
│   │   └── [...]
├── components/
│   ├── component-one/
│   │   ├── ComponentOne.tsx
│   │   └── ComponentOne.module.css
│   ├── component-two/
│   │   ├── ComponentTwo.tsx
│   │   └── ComponentTwo.module.css
│   └── [...]
├── lib/
│   ├── actions/
│   │   └── [...]
│   ├── helpers/
│   │   └── [...]
│   └── [...]
├── public/
│   └── [...]
├── styles/
│   └── [...]
├── utils/
│   └── [...]
├── .env.local
├── next.config.js
├── package.json
└── README.md
```

## File and Folder Naming Conventions


In NextJS, it is recommended to use lowercase letters and hyphens to separate words in file and folder names. This makes it easier to read and avoids confusion when working with different file types. For example, instead of using AboutUs.js, use about-us.js.


## Component Naming Conventions

When creating components in NextJS, it is best to use PascalCase for naming. This convention makes it easier to differentiate between components and regular HTML elements. For example, instead of using my-container, use MyContainer.

## Route Naming Conventions

Routes in NextJS should follow the same naming conventions as file and folder names. This makes it easier to identify routes and avoids confusion when navigating through your application. For example, instead of using /aboutUs, use /about-us.





