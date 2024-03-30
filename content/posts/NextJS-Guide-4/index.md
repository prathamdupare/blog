---
author: "Pratham Dupare"
title: "API Routes"
date: 2024-03-11
description: 'Basic to advance guide for Next.js'
tags: ["Web Development", "NextJs"]
thumbnail: null
tags: ["series", "docs"]
series: ["Next.js Guide"]
series_order: 4
---

## Introduction

Next.js is a full-stack framework that enables you to develop both the frontend and backend seamlessly. In contrast to using Express.js for building the backend, where you might need to run a separate server on a different port, Next.js eliminates this need.

Next.js employs a file-based routing system, making it convenient and efficient.

```javascript
const express = require("express");
const app = express();
const port = 3000;

app.get("/", (req, res) => {
  res.send("Hello World!");
});

app.listen(port, () => {
  console.log(`Example app listening on port ${port}`);
});
```

Note that in the traditional Express.js example, app.listen specifies the port to which it must listen, requiring it to be continuously running to handle requests.

Next.js covers all traditional backend features, including middlewares, parsing, authentication, and even serverless functions.

## Creating the API Route

Route Handlers allow you to create custom request handlers for a given route using the Web Request
and Response
APIs.

Route Handlers are defined in a `route.js|ts` file inside the `app` directory:

```javascript
//app/api/route.js
export const dynamic = "force-dynamic"; // defaults to auto
export async function GET(request) {}
```

Route Handlers can be nested inside the `app` directory, similar to `page.js` and `layout.js`. But there cannot be a `route.js` file at the same route segment level as `page.js`.

While Route Handlers can be nested inside the `app` directory, similar to `page.js` and `layout.js`, it's crucial to avoid having a `route.js` file at the same route segment level as `page.js`. A recommended practice is to keep routes separate in another folder, commonly in `/api/*`.

For instance, if you need a route at `/api/users`, create a `users` folder inside the `api` directory and then add a `route.js` file inside it. This route will correspond to `/api/users`.

This route will point to `/api/users`.

## Supported HTTP Methods

The following HTTP methods
are supported: `GET`, `POST`, `PUT`, `PATCH`, `DELETE`, `HEAD`, and `OPTIONS`. If an unsupported method is called, Next.js will return a `405 Method Not Allowed` response.

This is esentially everything you need.

To handle a `GET` request, you simply write a `GET` function inside the `route.js` file.

```javascript
export async function GET() {
  return Response.json("Hello, Next.js!");
}
```

You return the response as you would return from any regular express server.

For example ,

```javascript
//app/api/items/route.js
export async function GET() {
  const res = await fetch("https://data.mongodb-api.com/...", {
    headers: {
      "Content-Type": "application/json",
      "API-Key": process.env.DATA_API_KEY,
    },
  });
  const data = await res.json();

  return Response.json({ data });
}
```

Similarly, and within the same file, you can use all other `HTTP` verbs.

To witness this specific API in your browser, go to: `http://localhost:3000/app/api/items`.

That's it! It's simple and intuitive.
this is a test.
