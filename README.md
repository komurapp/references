# Useful links

## Ubuntu

TODO: pullout the desired commands to this section
- Fabio Akita's [Definitive Ubuntu's guide](https://www.youtube.com/watch?v=epiyExCyb2s)

- Most basic programs

- asdf

- Postgres

- Private/Public key; SSH key Ed25519

- tmux

- zsh

-vim

## Docker

- "Version in “./docker-compose.yml” is unsupported. You might be seeing this error because you're using the wrong Compose file version": [SOLUTION](https://stackoverflow.com/questions/42139982/version-in-docker-compose-yml-is-unsupported-you-might-be-seeing-this-error)

- Good explanation from [McLeod](https://github.com/GoesToEleven/golang-web-dev/tree/master/043_docker/01_about-containers)

- Installing Docker - [the painless way](https://linuxhint.com/install_docker_linux_mint/)

## Vim/Neovim

- my [.dotfiles](https://github.com/rongzinho/dotfiles) with bash, tmux, VS
  Code, nvim and git preferences.

## TypeScript

- Global installation using [yarn](https://classic.yarnpkg.com/en/docs/cli/global/)

- Include at your `zsh` file
> export PATH="$(yarn global bin):$PATH"
- Then, source it
> . ~/.zsh

### Simple server, with hot reload:
At your project's root folder:
> yarn init

to generate package configuration.

Answer the  prompted questions, then install it
> yarn add lite-server --dev
