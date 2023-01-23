# Readme

Bug reproduction for Remix v2 routing root index [issue](https://github.com/remix-run/remix/issues/5216)

This repo contains the "basic" example from the remix run examples repo and then the only change I have made is adding:

```
future: {
    v2_routeConvention: true
  }
```
to the `remix.config.js` file.

When running `npx remix routes` I then recieve:
`<Route path="index" file="routes/index.tsx" />` and the content from the `app/routes/index.tsx` does **not** show on the page.

If I rename the `index.tsx` file to `_index.tsx` and restart the dev server then the content shows corretly and `npx remix routes` comes back as:
`<Route index file="routes/_index.tsx" />`