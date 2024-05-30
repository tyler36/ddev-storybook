[![tests](https://github.com/ddev/ddev-addon-template/actions/workflows/tests.yml/badge.svg)](https://github.com/ddev/ddev-addon-template/actions/workflows/tests.yml) ![project is maintained](https://img.shields.io/maintenance/yes/2024.svg)

# ddev-storybook <!-- omit in toc -->

- [What is ddev-storybook?](#what-is-ddev-storybook)
- [Components of the repository](#components-of-the-repository)
- [Getting started](#getting-started)
- [Usage](#usage)
    - [Open Storybook](#open-storybook)
    - [Start Storybook server](#start-storybook-server)
- [Contributing](#contributing)

## What is ddev-storybook?

This addon makes it easier to work with Storybook 7 and DDEV.
It does this by:

- exposing Storybook on port 6006.
- adding a helper command.

[Storybook](https://storybook.js.org/) is "a frontend workshop for building UI components".
The addon assumes the developer is correctly installed and configured Storybook using the default port (`6006`).

## Components of the repository

- `config.storybook.yaml`: exposes the default Storybook port.
- `commands/host/storybook`: Helper command

## Getting started

1. Install the addon and restart DDEV.

```shell
ddev get tyler36/ddev-storybook
ddev restart
```
2. Install storybook if you haven't already. See the [Storybook get started page](https://storybook.js.org/docs/get-started/install) for instructions. E.g.
```shell
ddev exec npx storybook@latest init
```

## Usage

The helper function has 2 basic usage:

### Open Storybook

Use the following command to open Storybook in the default browser.

```shell
ddev storybook
```

### Start Storybook server

Use the following command to start the Storybook server.

```shell
ddev storybook -s
```

Alternatively,

```shell
ddev storybook --start
```

This command will try to run the "storybook" script from `package.json` in NPM.
If a `yarn.lock` file exists, it will run the command with YARN instead.

## Contributing

This addon was originally created to work with Drupal and [storybook](https://www.drupal.org/project/storybook) contrib module. It has _not_ been tested in other environments, although assuming Storybook defaults, it should work.

PRs, especially with automated tests are welcome.

**Contributed and maintained by [@tyler36](https://github.com/tyler36)**
