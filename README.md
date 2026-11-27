This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Getting Started

Create a **Regular Web Application** in the [Auth0 Dashboard](https://manage.auth0.com), then create `.env.local` in this project directory (not inside `src`):

```env
AUTH0_DOMAIN=your-tenant.auth0.com
AUTH0_CLIENT_ID=your-client-id
AUTH0_CLIENT_SECRET=your-client-secret
AUTH0_SECRET=your-generated-session-secret
APP_BASE_URL=http://localhost:3000
```

Get the domain, client ID, and client secret from the application's settings in the Auth0 Dashboard. Use the domain without `https://`. Generate a random session secret with `node -e "console.log(require('crypto').randomBytes(32).toString('hex'))"`, and replace `your-generated-session-secret` with its output. Keep `.env.local` private; it is ignored by Git.

In the Auth0 application settings, add `http://localhost:3000/auth/callback` to **Allowed Callback URLs** and `http://localhost:3000` to **Allowed Logout URLs**. Adjust these URLs and `APP_BASE_URL` if the app runs on a different port.

Then run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Restart the development server after changing `.env.local`. A missing `AUTH0_DOMAIN` causes the `DomainResolutionError` in the proxy.

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
