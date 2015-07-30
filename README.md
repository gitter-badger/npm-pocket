# NPM Pocket Guide For Busy People

## Definition

[NPM](https://www.npmjs.com/) Node Package Manager

## Purpose

Store, install, uninstall, update, Node packages from command line.

## Overview

NPM maintains a registry of Node packages and offers a command line interface (CLI) to manage packages. Packages can be installed globally, or locally (i.e. relative to your project folder).

*Source: https://docs.npmjs.com/getting-started/what-is-npm*

## Install

NPM comes with Node, so refer to [Node Pocket Guide](https://github.com/heyallan/node-pocket) for installation.

## Update

```shell
## update
$ npm cache clean
$ sudo npm install -g npm@latest

## If your npm is broken
$ curl -L https://www.npmjs.org/install.sh | sh
```

## Example

```shell
## create package.json
$ npm init

## install gulp (a package) globally
$ npm install --global gulp

## install gulp relative to project folder
$ npm install --save-dev gulp
```
The option `--save-dev` will save installation details to `package.json` automatically.

Packages installed locally are downloaded from NPM registry to a folder named `node_modules`.

When sharing a project whith colleagues you don't ship `node_modules` directory, but only `package.json` file. When receiving the project you (or your colleagues) just run `npm install` from their console and every package listed on `package.json` will be installed locally automatically. This allows lightweight sharing and setup. Basically you are sharing an "installer".

**Remember:** Directory `node_modules` should NOT be tracked by version control, only track/share/publish `package.json`.

*Source: https://docs.npmjs.com/getting-started/installing-npm-packages-locally*

## Reference
https://nodejs.org/api/
