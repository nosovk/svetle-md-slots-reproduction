# create-svelte

Everything you need to build a Svelte project, powered by [`create-svelte`](https://github.com/sveltejs/kit/tree/master/packages/create-svelte);

## Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

Before creating a production version of your app, install an [adapter](https://kit.svelte.dev/docs#adapters) for your target environment. Then:

```bash
npm run build
```

> You can preview the built app with `npm run preview`, regardless of whether you installed an adapter. This should _not_ be used to serve your app in production.

## Styles

We have different types of styles

### global styles

instead of prepending all with `global` we can put global styles to `src/app.scss` which will be applied unscoped to app.

### scoped styles

all components have scoped styles places inside component.

### global mixin

to use scss variables and mixins in scoped components we have to import them directly into each component. To avoid code bloat we import `./src/mixins.scss` to EVERY component. Never put anything that can compile to CSS in it, only mixins, scss vars etc.
