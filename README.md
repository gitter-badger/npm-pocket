# NPM: Pocket Guide For Busy People

## Definition

[NPM](https://www.npmjs.com/): Node Package Manager

## Purpose

Store, install, uninstall, update, Node packages from command line.

## Overview

NPM maintains a registry of Node packages. Offers a CLI (command line interface) to manage packages.

*Source: https://docs.npmjs.com/getting-started/what-is-npm*

## Install

NPM comes with Node, so refer to Node for installation.

See [Node](https://github.com/heyallan/node) (pocket guide)

## Update

```shell
## update
$ npm cache clean
$ sudo npm install -g npm@latest

## If your npm is broken
$ curl -L https://www.npmjs.org/install.sh | sh
```

## Example

Packages can be installed globally to be executed at any location, or locally to be executedonly inside project folder.

Node uses a `package.json` file to save details of what you have installed. NPM will use this file to remember your setup and follow your preferences.

```shell
## create package.json file to save details
$ npm init

## install gulp globally
$ npm install --global gulp

## install gulp in project folder and save details to package.json
$ npm install --save-dev gulp
```

*Source: https://docs.npmjs.com/getting-started/installing-npm-packages-locally*

## Reference
https://nodejs.org/api/
