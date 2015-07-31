# NPM Pocket Guide For Busy People

## Definition

[NPM](https://www.npmjs.com/) Node Package Manager

## Purpose

Store, install, uninstall, update, all Node packages (modules) from command line

## Overview

NPM maintains a registry of Node packages and offers a command line interface (CLI) to manage them. Packages can be installed globally and/or locally.

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
Options

`npm init` looks for an existing `package.json` befor creating a new one<br/>
`--global` installs the package's CLI globally, so it can be run from command line<br/>
`--save-dev` installs the package's API locally (to `node_modules`), so it can be consumed by other packages<br/>
`--save-dev` saves installation details to `package.json` automatically<br/>

## Also important

When deploying you don't ship `node_modules`, nor track it with Git, use `package.json` instead. When receiving the project you (or your colleagues) must run `npm install` from their console, and NPM will install every package listed on `package.json`. This allows lightweight sharing and reproducible setup. Basically you are sharing an "installer".

*Source: https://docs.npmjs.com/getting-started/installing-npm-packages-locally*

## Reference
https://nodejs.org/api/
