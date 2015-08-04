# NPM Pocket Guide For Busy People

## Definition

[NPM](https://www.npmjs.com/) Node Package Manager

## Purpose

Store, install, uninstall, update, any Node packages (modules)

## Overview

NPM maintains a registry of Node packages at [npmjs.org](npmjs.org), and offers a command line interface (CLI) to manage them from your local computer, or server.

*Source: https://docs.npmjs.com/getting-started/what-is-npm*

## Install

NPM comes with Node, so refer to [Node Pocket Guide](https://github.com/heyallan/node-pocket) for installation.

## Example

```shell
## create package.json
$ npm init

## install gulp (a package) globally
$ npm install --global gulp

## install gulp locally as one of your project's dependencies
$ npm install --save-dev gulp
```

Options:

- `npm init` looks for an existing `package.json` file, if not, it creates a new one
- `npm install` installs the package's API to `node_modules` folder, so Node can run it as a javascript module
- `--global` installs the package's CLI globally, so Node can run it as a CLI
- `--save-dev` saves all package's details to `package.json` so you can keep track of all installations

*See all npm install options https://docs.npmjs.com/cli/install*

## Also important

When deploying a website, you don't ship `node_modules` folder, nor track it with Git, use `package.json` instead. When cloning the project you (or your colleagues) must run `npm install` from their console, and NPM will install every package listed on `package.json`. This allows lightweight sharing and reproducible setup. Basically you are sharing an "installer" in `package.json`.

*Source: https://docs.npmjs.com/getting-started/installing-npm-packages-locally*

## Update

```shell
## update npm
$ npm cache clean
$ sudo npm install -g npm@latest

## If your npm is broken
$ curl -L https://www.npmjs.org/install.sh | sh
```

## Reference
https://nodejs.org/api/
