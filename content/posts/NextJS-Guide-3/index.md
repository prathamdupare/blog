---
author: "Pratham Dupare"
title: "Components and Optimisations"
date: 2024-03-08
description: 'Basic to advance guide for Next.js'
tags: ["Web Development", "NextJs"]
thumbnail: null
tags: ["series", "docs"]
series: ["Next.js Guide"]
series_order: 3
---

## Introduction

Next.js comes with a variety of built-in optimizations designed to improve your application's speed and Core Web Vitals
.

## Built-in Components

### 1. Images Component:

- Utilizes the native `<img>` element.
- Optimizes image performance by implementing lazy loading.
- Automatically resizes images based on the device size for improved responsiveness.

```jsx
//app/page.js
import Image from "next/image";

export default function Page() {
  return (
    <Image
      src="/profile.png"
      width={500}
      height={500}
      alt="Picture of the author"
    />
  );
}
```

The Image Component requires the following properties: `src`, `width`, `height`, and `alt`.

### 2. Link Component:

The `<Link>` component in Next.js is a React component that extends the HTML `<a>` element. It plays a crucial role in providing prefetching and enabling client-side navigation between routes. This component serves as the primary means of navigating between routes in a Next.js application.

- Built on the native `<a>` tags.
- Prefetches pages in the background, enhancing page transition speed.
- Facilitates faster and smoother navigation between pages.

```jsx
import Link from "next/link";

export default function Page() {
  return <Link href="/dashboard">Dashboard</Link>;
}
```

`href` (required)  
The path or URL to navigate to.

```jsx
<Link href="/dashboard">Dashboard</Link>
```

- **Linking to Dynamic Routes**

```jsx
//app/blog/page.js
import Link from "next/link";

function Page({ posts }) {
  return (
    <ul>
      {posts.map((post) => (
        <li key={post.id}>
          <Link href={`/blog/${post.slug}`}>{post.title}</Link>
        </li>
      ))}
    </ul>
  );
}
```

For example, you can generate a list of links to the dynamic route `app/blog/[slug]/page.js`:

### 3. Scripts Component:

This is self-explanatory, this let's you run scripts for a specific components.

- Implemented with the native `<script>` tags.
- Provides control over the loading and execution of third-party scripts.
- Enables efficient management of external scripts for better overall performance.

```jsx
import Script from "next/script";

export default function Dashboard() {
  return (
    <>
      <Script src="https://example.com/script.js" />
    </>
  );
}
```

**Required Props for Script Component in Next.js**

The `<Script>` component in Next.js requires the following property:

- **src:**
  - Type: String
  - Description: A path string specifying the URL of an external script. This can be either an absolute external URL or an internal path.
  - Requirement: The `src` property is required unless an inline script is used.

**Optional Props** :

| Prop       | Example                           | Type     | Required                              |
| ---------- | --------------------------------- | -------- | ------------------------------------- |
| `src`      | `src="http://example.com/script"` | String   | Required unless inline script is used |
| `strategy` | `strategy="lazyOnload"`           | String   | -                                     |
| `onLoad`   | `onLoad={onLoadFunc}`             | Function | -                                     |
| `onReady`  | `onReady={onReadyFunc}`           | Function | -                                     |
| `onError`  | `onError={onErrorFunc}`           | Function | -                                     |

For a comprehensive guide on Next.js components, refer to the [Api Reference/Components](https://nextjs.org/docs/app/api-reference/components) section of the official Next.js documentation.

## Static Assets

The Next.js `/public` folder serves as a convenient location for hosting static assets such as images, fonts, and other files.

Files stored within the `/public` directory can be efficiently cached by Content Delivery Network (CDN) providers. This caching mechanism enhances the delivery speed of assets to users, resulting in a smoother browsing experience.

## Metadata

**Next.js Metadata API for Improved SEO and Shareability**

Next.js provides a Metadata API that allows you to define your application's metadata, including meta and link tags inside the HTML head element. This is crucial for enhancing SEO and improving web shareability.

There are two methods to add metadata to your application:

1. **Config-based Metadata:**

   - Export a static metadata object or a dynamic `generateMetadata` function in a `layout.js` or `page.js` file.

2. **File-based Metadata:**
   - Add static or dynamically generated special files to route segments.

Regardless of the method chosen, Next.js will automatically generate the relevant `<head>` elements for your pages. Additionally, you can create dynamic Open Graph (OG) images using the `ImageResponse` constructor for a more customized and engaging web sharing experience.

To define static metadata, export a Metadata object from a `layout.js`(we have already seen in previous chapter) or static `page.js` file.

```
export const metadata = {
  title: '...',
  description: '...',
}

export default function Page() {}
```

These components and elements cover the fundamental requirements for constructing a speedy and responsive Next.js application.
