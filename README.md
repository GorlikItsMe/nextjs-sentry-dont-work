# Update: It works now
https://github.com/getsentry/sentry-javascript/issues/13270

---

# nextjs + sentry dont work

For some reason sentry cant upload sourcemaps during buildtime. Because of that, you cant see the source code in the sentry dashboard.

```bash
# create a new nextjs project
npx create-next-app 

# install sentry
npx @sentry/wizard@latest -i nextjs

# add silent: false in next.config.mjs to see what is happening

# Try build
npm run build
```

And you will:

```
[@sentry/nextjs - Node.js] Info: Sending telemetry data on issues and performance to Sentry. To disable telemetry, set `options.telemetry` to `false`.
[@sentry/nextjs - Node.js] Warning: Didn't find any matching sources for debug ID upload. Please check the `sourcemaps.assets` option.
[@sentry/nextjs - Edge] Info: Sending telemetry data on issues and performance to Sentry. To disable telemetry, set `options.telemetry` to `false`.
[@sentry/nextjs - Edge] Warning: Didn't find any matching sources for debug ID upload. Please check the `sourcemaps.assets` option.
[@sentry/nextjs - Client] Info: Sending telemetry data on issues and performance to Sentry. To disable telemetry, set `options.telemetry` to `false`.
[@sentry/nextjs - Client] Warning: Didn't find any matching sources for debug ID upload. Please check the `sourcemaps.assets` option.
```

-----------


This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.
