# Svelte TS Starter

This Svelte TS starter template provides a foundation for developing with Svelte and Vite, including preconfigured support for TailwindCSS, Flowbite-Svelte, and Svelte-Spa-Router. Additionally, it includes a sample implementation of fetching data from a backend API, making it easy to integrate with your own server-side infrastructure.

## Installation

```bash
git clone git@github.com:shinokada/svelte-ts-starter.git my-app
cd my-app
pnpm i
```

## Backend API env value

Update your backend API value in `.env`:

```text
API_ENDPOINT=http://localhost:3000/api
API_SECRET=1234
```

## Start a local server

```bash
npm run dev
```

## How to use this for GitHub page

There is the `github-page` branch. Please note that it is not gh-pages.
Checkout to this branch and install packages, build and deploy.

```
git checkout github-page
pnpm i
npm run build
npm run deploy
```

This will deploy your GitHub page to `https://<username>.github.io/<repository name>` URL. Don’t forget to change the username and repository name to your personal Github username and repository.
It may take a couple of minutes. You can check the progress in GitHub Actions tab.