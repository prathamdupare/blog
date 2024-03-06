---
author: "Pratham Dupare"
title: "Server components and Client Components in Next.js"
date: 2024-03-06
description: "Basic to advance guide for Next.js"
slug: "series"
tags: ["Web Development", "NextJs"]
thumbnail: null
series: ["Next.js Guide"]
series_order: 2
---

## Server components

By default, Next.js uses Server Components. This makes server rendering possible without any configuration and you can opt into using Client Components when needed.

Reacr Server Components allow you to write UI that can be rendered and optionally cached on the server.

## Why Server Rendering

There are a lot of benefits of server side rendering such as :

- **Data Fetching**: Fetching data on the server improves performance by reducing client-side data retrieval time and the number of requests.

- **Security: Keeping** sensitive data and logic on the server, such as tokens and API keys, prevents exposure to the client, enhancing security.

- **Caching** : Server-side rendering allows for caching, improving performance and reducing costs by reusing results across requests and users.

- **Bundle Sizes**: Large dependencies impacting client bundles are moved to the server, benefiting users with slower internet or less powerful devices.

- **Initial Page Load and FCP**: Server-generated HTML enables immediate page viewing without waiting for client-side JavaScript execution.

- **SEO and Shareability**: Rendered HTML aids search engine indexing and social network previews for better SEO and shareability.

- **Streaming**: Server Components enable rendering in chunks, allowing users to see parts of the page earlier, enhancing the user experience.

## Rendering

So how are server components rendered?

On the server, Next.js uses React's API to start rendering. When requested on client, the html is used to immidiately show a fast non-interactive preview on the route.

### Static and dynamic rendering

Static Rendering (Default):
Routes are pre-rendered at build time or in the background, then cached and stored. This is great for content that doesn't change per user, like static blog posts or product pages.

Dynamic Rendering:
Routes are generated for each user when requested. This is useful for content that is personalized or relies on information like cookies or URL parameters, which can only be known at the time of the request.

As a developer you don't have to choose static or dynamic rendering.

## Client components

Client Components allow you to write interactive UI that is prerenderd on the server and use client JavaScript to run in the browser.

_Benefits_ of doing the rendering on the client are :

- You can use states, use state, effects and event listners on client components and they can provide immidiate feedback to the user and update the UI on client side.
- Browser APIs like geolocation and localStorage can be accesed.

## Using Client Components in Next.js

To use a Client Components, you can use the React `"use client"` directive at the top of a file.

{{< highlight html "linenos=table,hl_lines=2" >}}

```
'use client'

import { useState } from 'react'

export default function Counter() {
  const [count, setCount] = useState(0)

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>Click me</button>
    </div>
  )
}
```

{{< /highlight >}}

That is all you need to convert server components to client componets.

> **Note** - If you use state, effects, browser APIs without specifying the client component by `"use client"`, Next.js will thorow an error.

## Full page load

To optimize the initial page load, Next.js will use React's APIs to render a static HTML preview on the server for both Client and Server Components. This means, when the user first visits your application, they will see the content of the page immediately, without having to wait for the client to download, parse, and execute the Client Component JavaScript bundle.

# Conclusion

Server and Client Components enhance website performance, conserve data, and are especially advantageous for low-powered devices. You have the flexibility to choose when to employ client components as needed!
