# Developer's References

A compilation of relative common tasks/problems of daily web development on Linux.

Simplifies the start up on Linux-based machines

> Mostly tested on **Mint**, therefore **Ubuntu** users can also follow this.

Most of projects had used at least one of the following: React, Flutter, Go, Postgres or Docker.

## Ubuntu

TODO: pullout the desired commands to this section
- Fabio Akita's [Definitive Ubuntu's guide](https://www.youtube.com/watch?v=epiyExCyb2s)

- Most basic programs

- asdf

- Postgres

- Private/Public key; SSH key Ed25519

## Docker

- "Version in “./docker-compose.yml” is unsupported. You might be seeing this error because you're using the wrong Compose file version": [SOLUTION](https://stackoverflow.com/questions/42139982/version-in-docker-compose-yml-is-unsupported-you-might-be-seeing-this-error)

- Good explanation from [McLeod](https://github.com/GoesToEleven/golang-web-dev/tree/master/043_docker/01_about-containers)

- Installing Docker - [the painless way](https://linuxhint.com/install_docker_linux_mint/)

## TypeScript
For testing purposes, there's an official [sandbox](https://www.typescriptlang.org/play/index.html)
### Installation

- Global installation using [yarn](https://classic.yarnpkg.com/en/docs/cli/global/)

- Include at your `zsh` file, if **not** automatically detected
```
export PATH="$(yarn global bin):$PATH"
```
- Then, source it
```
. ~/.zsh
```

### Simple server, with *hot reload* and *watch mode*:
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
