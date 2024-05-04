---
title: "Full Stack Framework for Next JS Setup"
seoTitle: "T3 Framework for Full Stack Next JS Setup"
datePublished: Sat May 04 2024 19:53:26 GMT+0000 (Coordinated Universal Time)
cuid: clvsiuhjm000009mmczxi6sly
slug: full-stack-framework-for-next-js-setup
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/vetW6Y89T3w/upload/a5ab40b79f7791ced24390305a189193.jpeg
tags: programming-blogs, programming-school, t3, t3stack

---

## [The T3 Stack](https://create.t3.gg/en/introduction#the-t3-stack)

The *“T3 Stack”* is a web development stack made by [Theo↗](https://twitter.com/t3dotgg) focused on simplicity, modularity, and full-stack typesafety.

The core pieces are [**Next.js**↗](https://nextjs.org/) and [**TypeScript**↗](https://typescriptlang.org/). [**Tailwind CSS**↗](https://tailwindcss.com/) is almost always included. If you’re doing anything resembling backend, [**tRPC**↗](https://trpc.io/), [**Prisma**↗](https://prisma.io/), and [**NextAuth.js**↗](https://next-auth.js.org/) are great additions too.

You may have noticed that there are a… lot of pieces. That’s by design. Swap pieces in and out as you need - this stack is modular at its core

## [So… what is create-t3-app? A template?](https://create.t3.gg/en/introduction#so-what-is-create-t3-app-a-template)

Kind of? `create-t3-app`is a CLI built by seasoned T3 Stack devs to streamline the setup of a modular T3 Stack app. This means each piece is optional, and the “template” is generated based on your specific needs.

After countless projects and many years on this tech, we have lots of opinions and insights. We’ve done our best to encode them into this CLI.

This is **NOT** an all-inclusive template. We **expect** you to bring your own libraries that solve the needs of **YOUR** application. While we don’t want to prescribe solutions to more specific problems like state management and deployment, we [do have some recommendations listed here](https://create.t3.gg/en/other-recs).

---

# Setup Create T3 App

Now you knew what is `create-t3-app`

So Now we will create our first t3 app

first you must run the command that creates the app structure

```bash
# npm
npm create t3-app@latest

# yarn
yarn create t3-app

# pnpm
pnpm create t3-app@latest

# bun
bun create t3-app@latest
```

  
Answer your questions as you want but answer it as we answer it to complete the post with us:

```bash
   ___ ___ ___   __ _____ ___   _____ ____    __   ___ ___
  / __| _ \ __| /  \_   _| __| |_   _|__ /   /  \ | _ \ _ \
 | (__|   / _| / /\ \| | | _|    | |  |_ \  / /\ \|  _/  _/
  \___|_|_\___|_/‾‾\_\_| |___|   |_| |___/ /_/‾‾\_\_| |_|


│
◇  What will your project be called?
│  first-t3-app
│
◇  Will you be using TypeScript or JavaScript?
│  TypeScript
│
◇  Will you be using Tailwind CSS for styling?
│  Yes
│
◇  Would you like to use tRPC?
│  No
│
◇  What authentication provider would you like to use?
│  NextAuth.js
│
◇  What database ORM would you like to use?
│  Prisma
│
◇  Would you like to use Next.js App Router?
│  Yes
│
◇  What database provider would you like to use?
│  PostgreSQL
│
◇  Should we initialize a Git repository and stage the changes?
│  Yes
│
◇  Should we run 'npm install' for you?
│  Yes
│
◇  What import alias would you like to use?
│  @/
```

## Folder Structure

Command `npm create t3-app@latest` Creates some folder each of them have a reason for creating it so let's discover why these folders have created:

The Folder Structure:

```bash
.
├─ public
│  └─ favicon.ico
├─ prisma
│  └─ schema.prisma
├─ src
│  ├─ env.js
│  ├─ pages
│  │  ├─ _app.tsx
│  │  ├─ api
│  │  │  └─ auth
│  │  │     └─ [...nextauth].ts
│  │  └─ index.tsx
│  ├─ server
│  │  ├─ auth.ts
│  │  └─ db.ts
│  └─ styles
│     └─ globals.css
├─ .env
├─ .env.example
├─ .eslintrc.cjs
├─ .gitignore
├─ next-env.d.ts
├─ next.config.js
├─ package.json
├─ postcss.config.cjs
├─ prettier.config.js
├─ README.md
├─ tailwind.config.ts
└─ tsconfig.json
```

### [`prisma`](https://create.t3.gg/en/folder-structure?packages=nextauth%2Cprisma%2Ctailwind#prisma)

The `prisma` folder contains the `schema.prisma` file which is used to configure the database connection and the database schema. It is also the location to store migration files and/or seed scripts, if used. See [Prisma usage](https://create.t3.gg/en/usage/prisma) for more information.

### [`public`](https://create.t3.gg/en/folder-structure?packages=nextauth%2Cprisma%2Ctailwind#public)

The `public` folder contains static assets that are served by the web server. The `favicon.ico` file is an example of a static asset.

### [`src/env`](https://create.t3.gg/en/folder-structure?packages=nextauth%2Cprisma%2Ctailwind#srcenv)

Used for environment variable validation and type definitions - see [Environment Variables](https://create.t3.gg/en/usage/env-variables).

### [`src/pages`](https://create.t3.gg/en/folder-structure?packages=nextauth%2Cprisma%2Ctailwind#srcpages)

The `pages(app)` folder contains all the pages of the Next.js application. The `index.tsx` file at the root directory of `/pages` is the homepage of the application. The `_app.tsx` file is used to wrap the application with providers. See [Next.js documentation↗](https://nextjs.org/docs/basic-features/pages) for more information.

#### [`src/pages/api`](https://create.t3.gg/en/folder-structure?packages=nextauth%2Cprisma%2Ctailwind#srcpagesapi)

The `api` folder contains all the API routes of the Next.js application. See [Next.js Api Routes Docs↗](https://nextjs.org/docs/api-routes/introduction) for info on api routes.

#### [`src/pages/api/auth/[...nextauth].ts`](https://create.t3.gg/en/folder-structure?packages=nextauth%2Cprisma%2Ctailwind#srcpagesapiauthnextauthts)

The `[...nextauth].ts` file is the NextAuth.js authentication slug route. It is used to handle authentication requests. See [NextAuth.js usage](https://create.t3.gg/en/usage/next-auth) for more information on NextAuth.js, and [Next.js Dynamic Routes Docs↗](https://nextjs.org/docs/routing/dynamic-routes) for info on catch-all/slug routes.

### [`src/server`](https://create.t3.gg/en/folder-structure?packages=nextauth%2Cprisma%2Ctailwind#srcserver)

The `server` folder is used to clearly separate server-side code from client-side code.

#### [`src/server/db.ts`](https://create.t3.gg/en/folder-structure?packages=nextauth%2Cprisma%2Ctailwind#srcserverdbts)

The `db.ts` file is used to instantiate the Prisma client at global scope. See [Prisma usage](https://create.t3.gg/en/usage/prisma#prisma-client) and [best practices for using Prisma with Next.js↗](https://www.prisma.io/docs/guides/database/troubleshooting-orm/help-articles/nextjs-prisma-client-dev-practices) for more information.

### [`src/styles`](https://create.t3.gg/en/folder-structure?packages=nextauth%2Cprisma%2Ctailwind#srcstyles)

The `styles` folder contains the global styles of the application.

### [`.env`](https://create.t3.gg/en/folder-structure?packages=nextauth%2Cprisma%2Ctailwind#env)

The `.env` file is used to store environment variables. See [Environment Variables](https://create.t3.gg/en/usage/env-variables) for more information. This file should **not** be committed to git history.

### [`.env.example`](https://create.t3.gg/en/folder-structure?packages=nextauth%2Cprisma%2Ctailwind#envexample)

The `.env.example` file shows example environment variables based on the chosen libraries. This file should be committed to git history.

### [`.eslintrc.cjs`](https://create.t3.gg/en/folder-structure?packages=nextauth%2Cprisma%2Ctailwind#eslintrccjs)

The `.eslintrc.cjs` file is used to configure ESLint. See [ESLint Docs↗](https://eslint.org/docs/latest/user-guide/configuring/configuration-files) for more information.

### [`next-env.d.ts`](https://create.t3.gg/en/folder-structure?packages=nextauth%2Cprisma%2Ctailwind#next-envdts)

The `next-env.d.ts` file ensures Next.js types are picked up by the TypeScript compiler. **You should not remove it or edit it as it can change at any time.** See [Next.js Docs↗](https://nextjs.org/docs/basic-features/typescript#existing-projects) for more information.

### [`next.config.mjs`](https://create.t3.gg/en/folder-structure?packages=nextauth%2Cprisma%2Ctailwind#nextconfigmjs)

The `next.config.mjs` file is used to configure Next.js. See [Next.js Docs↗](https://nextjs.org/docs/api-reference/next.config.js/introduction) for more information. Note: The .mjs extension is used to allow for ESM imports.

### [`postcss.config.cjs`](https://create.t3.gg/en/folder-structure?packages=nextauth%2Cprisma%2Ctailwind#postcssconfigcjs)

The `postcss.config.cjs` file is used for Tailwind PostCSS usage. See [Tailwind PostCSS Docs↗](https://tailwindcss.com/docs/installation/using-postcss) for more information.

### [`prettier.config.mjs`](https://create.t3.gg/en/folder-structure?packages=nextauth%2Cprisma%2Ctailwind#prettierconfigmjs)

The `prettier.config.mjs` file is used to configure Prettier to include the prettier-plugin-tailwindcss for formatting Tailwind CSS classes. See the [Tailwind CSS blog post↗](https://tailwindcss.com/blog/automatic-class-sorting-with-prettier) for more information.

### [`tsconfig.json`](https://create.t3.gg/en/folder-structure?packages=nextauth%2Cprisma%2Ctailwind#tsconfigjson)

The `tsconfig.json` file is used to configure TypeScript. Some non-defaults, such as `strict mode`, have been enabled to ensure the best usage of TypeScript for Create T3 App and its libraries. See [TypeScript Docs↗](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html) or [TypeScript Usage](https://create.t3.gg/en/usage/typescript) for more information.

### [`drizzle.config.ts`](https://create.t3.gg/en/folder-structure?packages=nextauth%2Cprisma%2Ctailwind#drizzleconfigts)

The `drizzle.config.ts` file is used to configure drizzle kit. See [the documentation↗](https://orm.drizzle.team/kit-docs/config-reference) for more information.

Now, the end of our article don't forget to follow, like and support us with a comment 💖