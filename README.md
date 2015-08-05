# NPM Pocket Guide For Busy People

## Definition

[NPM](https://www.npmjs.com/) Node Package Manager

## Purpose

Store, install, uninstall, update, any Node packages (modules)

## Overview

NPM maintains a registry of Node packages at [npmjs.org](npmjs.org), and offers a command line interface (CLI) to manage them from your local computer, or server.

**Important:**
- You don't need a *node-based* project to used NPM. Installing node just for NPM is also ok
- For using node on the web, you'll need a web hosting provider with node support, [DigitalOcean](https://www.digitalocean.com/?refcode=adf3cbb076be) for instance
- You might not need a web hosting privider with node support after all, using node/npm for tasks like compilation can be done locally, and then deploy processed files, it depends on what you want node for

*Source: https://docs.npmjs.com/getting-started/what-is-npm*

## Install

NPM comes with Node, see [Node Pocket Guide](https://github.com/heyallan/node-pocket)

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
https://www.npmjs.com/
