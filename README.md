# ts-types-starter-kit

Example of typescript types package.

## How does it works?

To use our types as package we need to compile it to the `.d.ts` a.k.a declarations and then push it to the registry.

1) Setup `tsconfig.json`
    - `"declaration": true` - activating declarations in our project.
    - `"emitDeclarationOnly": true` - allows to get only typings from our code.
    - `"declarationDir": "./dist"` - directory for declarations output

2) Create `index.ts` outside `src` folder.

Allows us to export all code from src.

3) Build

## How to use it?

1) Add `.ts` or `.d.ts` files to the `src` folder.
2) Run `build` script from package.json or via command line with _your package manager_:

```bash
npm run build
```

```bash
yarn build
```

```bash
pnpm build
```

3) Inspect compiled types declarations in the `dist` folder.

## How to publish to registry?

I added files for npm registry. You can safely delete it or replace.

1) Login:

```bash
npm login
```

2) Publish:

```bash
npm publish --access public
```

_NOTE:_ Sometimes you need to provide login token or something similar. Remember to delete it from your project.

## Links

- [How to publish packages to npm (the way the industry does things)
](https://zellwk.com/blog/publish-to-npm/)

- [How to Publish Your First npm Package](https://medium.com/@bretcameron/how-to-publish-your-first-npm-package-b224296fc57b)