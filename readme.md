# Pikapeo Portfolio

## Direct Sanity connection (without Netlify)

1. Open your Sanity project in the dashboard.
2. Go to Project settings -> API -> copy the Project ID and Dataset.
3. In [index.html](index.html), replace `YOUR_PROJECT_ID` in the `sanityConfig` object with your actual project ID.
4. Open the site locally and the page will try to fetch content from Sanity.
5. If no project is configured yet, the page will keep using the local fallback data.

Example:

```js
const sanityConfig = {
  projectId: 'abc123de',
  dataset: 'production',
  useCdn: true,
  apiVersion: '2026-10-20'
};
```

> The Sanity organization URL `https://www.sanity.io/organizations/op24718py` is the organization-level page, not the project ID. You need the actual project ID from the project settings.

## Run Sanity Studio locally

```bash
cd sanity
npx sanity dev
```

Then open http://localhost:3333
