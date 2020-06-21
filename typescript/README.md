# TypeScript
For testing purposes, there's an official [sandbox](https://www.typescriptlang.org/play/index.html).
## Installation

- Global installation using [yarn](https://classic.yarnpkg.com/en/docs/cli/global/)

- Include at your `zsh` file, if **not** automatically detected
```
export PATH="$(yarn global bin):$PATH"
```
- Then, source it
```
. ~/.zsh
```

## Simple server, with *hot reload* and *watch mode*:
i.e. changing `.ts` files will update your `.js` generated files and trigger an reload of your server. *That's beautiful*.

- At your project's root folder
```
yarn init
```

	to generate package configuration.

	> Note yarn will create `package.json`, `package-lock.json` and `node_modules/`.

- Answer the  prompted questions, then install it
```
yarn add lite-server --dev
```

- Create the `start` script by adding `"start": "lite-server"` to `"scripts"`, inside `package.json`.

	It should looks like this
```json
{
    "name": "some-typescript-project",
    "version": "1.0.0",
    "main": "app.js",
    "license": "MIT",
    "scripts": {
      "start": "lite-server"
    },
    "devDependencies": {
      "lite-server": "^2.5.4"
    }
}
```

- Open another terminal and config TS compiler
```
tsc --init
```

	> Note that tsc generates an configuration file `tsconfig.json`.

	then start *watch mode*
```
tsc -w
// or
tsc --watch
```

## Debugging at the browser

- Set `"sourceMap": true` at `tsconfig.json` to see `.ts` files at `Sources` tab.

	> It will generate `.js.map` files to each `.ts` files.

