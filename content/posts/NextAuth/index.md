---
author: "Pratham Dupare"
title: NextJS and NextAuth guide
date: 2024-03-03
description: "Simple guide for NextJS and NextAuth setup"
tags: ["Android", "html"]
thumbnail: ""
---

# Introduction

NextAuth.js is a complete open-source authentication solution for Next.js applications, and it is currently my favorite solution for adding authentication. It doesn't set up everything like Clerk in 7 minutes but also gives you control over everything and makes it really easy!

It's specifically designed to work seamlessly with Next.js and Serverless architectures.

# Getting Started

## Install NextAuth

```bash
npm install next-auth
```

#### Note -

I will be using the latest version of Next.js 14.0 or above with the app router.

Next.js 13.2 introduced Route Handlers, the preferred way to handle REST-like requests in App Router (app/).

You can initialize NextAuth with a Route Handler too, similar to API Routes.

```javascript
# /app/api/auth/[...nextauth]/route.js

import NextAuth from "next-auth"

const handler = NextAuth({
...
})

export { handler as GET, handler as POST }
```

Now, let's provide options to this, specifying the providers for sign-in.

Create a separate file for our options.

Create the options.js file in the same directory as the route.

For this tutorial, we'll use the Github Provider.

```
# /app/api/auth/[...nextauth]/options.js

export const options = {
providers: []
}
```

## Providers

An array of authentication providers for signing in (e.g., Google, Facebook, Twitter, GitHub, Email, etc.) in any order. This can be one of the built-in providers or an object with a custom provider.

For now, we'll stick to the default settings, but there are numerous customization options available.

We can use Credentials for login as well as Providers that support OAuth like Google, Github, etc.

Refer to the NextAuth documentation for a comprehensive list of providers.

Now, set up the secret string required by NextAuth:

To generate a random string, run this command in your terminal:

```
openssl rand -base64 32
```

Now, create a .env.local file on the same level as the package.json file (i.e., the root directory) and paste the generated string:

```

# .env.local

NEXTAUTH_SECRET=2Imue0dkSptxssYHeYU5WOWrpFESkq++SWbG/ItyYT4=
//replace this with your generated stirng

```

## Setting up Github

You'll need a GitHub account for this.

Go to https://github.com/settings/apps

Click on 'OAuth Apps' and then 'New OAuth App'

Provide an Application name and set the homepage URL as http://localhost:3000 (for the dev environment; change it when deploying).

In Authorization callback URL: http://localhost:3000/api/auth/callback/github

Click 'Register application'.

Copy the Client ID, generate the secret, and confirm access.

Add Client ID and Client secret to the .env.local file:

```
# .env.local

NEXTAUTH_SECRET=2Imue0dkSptxssYHeYU5WOWrpFESkq++SWbG/ItyYT4=
//replace this with your generated stirng

GITHUB_SECRET=74f7032f71a995401fasdfads9b870b255e6c18159b
GITHUB_ID=0c384680asdfasfcb9c61
```

## Options

First, import GitHubProvider and CredentialsProvider from next-auth/providers/credentials

```javascript
# /app/api/auth/[...nextauth]/options.js

import GitHubProvider from "next-auth/providers/github";
import CredentialsProvider from "next-auth/providers/credentials";

export const options = {
    providers: []
}
```

Now in the providers array add GitHubProvider and set id and secret:

```
# /app/api/auth/[...nextauth]/options.js

import GitHubProvider from "next-auth/providers/github";
import CredentialsProvider from "next-auth/providers/credentials";

export const options = {
    providers: [
        GitHubProvider({
            clientId: process.env.GITHUB_ID,
            clientSecret: process.env.GITHUB_SECRET,
    }),
   ],
}
```

add CredentialsProvider.

```
# /app/api/auth/[...nextauth]/options.js

import GitHubProvider from "next-auth/providers/github";
import CredentialsProvider from "next-auth/providers/credentials";
export const options = {
    providers: [
        GitHubProvider({
            clientId: process.env.GITHUB_ID,
            clientSecret: process.env.GITHUB_SECRET,
    }),
    CredentialsProvider({
      name: "Credentials",
      credentials: {
        username: {
          label: "Username:",
          type: "text",
          placeholder: "your-cool-username",
        },
        password: {
          label: "Password:",
          type: "password",
          placeholder: "your-awesome-password",
        },
      },
      async authorize(credentials) {
        // This is where you need to retrieve user data
        // to verify with credentials
        // Docs: https://next-auth.js.org/configuration/providers/credentias
        const user = { id: "42", name: "Dave", password: "nextauth" };

        if (
          credentials?.username === user.name &&
          credentials?.password === user.password
        ) {
          return user;
        } else {
          return null;
        }
      },
    }),
   ],
}
```

The CredentialsProvider is configured with a name, "Credentials," and includes credential fields for username and password with associated labels, types, and placeholders.

Within the authorize function of the CredentialsProvider configuration, a simple authentication logic is demonstrated. A hardcoded user object is compared with the provided credentials. If there's a match, the user object is returned; otherwise, null is returned.

In a real-world scenario, the authorize function would typically interact with a database or an external service for dynamic credential validation. This example serves as a concise illustration of setting up a custom CredentialsProvider in NextAuth.js for username and password authentication.

Now, we just need to import and set options in the route.js file:

```javascript
# /app/api/auth/[...nextauth]/route.js

import NextAuth from "next-auth";
import { options } from "./options";

const handler = NextAuth(options);

export { handler as GET, handler as POST };

```

Then run the app:

```
npm run dev
```

Test it by making a GET request on Postman.
Open Postman and make a GET request to the URL: http://localhost:3000/api/auth/providers

You should get a response like:

```json
{
  "github": {
    "id": "github",
    "name": "GitHub",
    "type": "oauth",
    "signinUrl": "http://localhost:3000/api/auth/signin/github",
    "callbackUrl": "http://localhost:3000/api/auth/callback/github"
  },
  "credentials": {
    "id": "credentials",
    "name": "Credentials",
    "type": "credentials",
    "signinUrl": "http://localhost:3000/api/auth/signin/credentials",
    "callbackUrl": "http://localhost:3000/api/auth/callback/credentials"
  }
}
```

This covers almost everything needed to set up authentication. Now, let's inform NextAuth about which pages are protected.
The simplest way is using NextJS middleware. This middleware runs between server and client requests:

Let's do it!

Create a 'middleware.js' file on the same level as the 'app' directory

```javascript
# /middleware.js

export { default } from "next-auth/middleware";
```

This will protect everything in your app, even the home page. You can check this by going to http://localhost:3000 and you will be redirected to the signup page.

If you want to protect only some pages in your app, add this one line to your middleware.js

```javascript
# /middleware.js

export { default } from "next-auth/middleware";
export const config = { matcher: ["/dashboard"] };

```

For example, this will only protect the '/dashboard' route.

And there you go! This is all you need to have basic authentication on your project.

## Bonus

If you want to have certain information on the client side to show email, name, or profileImage, you can get that from useSession()

For example:

```javascript

# /navbar.jsx

"use client";

import React from "react";

import { Button } from "./ui/button";
import Image from "next/image";
import Link from "next/link";

import { useSession } from "next-auth/react";

const Navbar = () => {
  const { data: session } = useSession();
  return (
    <div>
      {!session ? (
        <Button>
          <Link href="/api/auth/signin">LogIn</Link>
        </Button>
      ) : (
        <div className="flex gap-3 items-center">
          <Image
            className="rounded-full"
            alt="hlh"
            width={30}
            height={30}
            src={session.user?.image}
          />
          <Button>
            <Link href="/api/auth/signout">SignOut</Link>
          </Button>
        </div>
      )}
    </div>
  );
};
```

Thanks for reading!

> 'Jack of all trades master of none, though oftentimes better than master of one.'
