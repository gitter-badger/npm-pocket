# NPM For Busy People

## Definition
NPM: Node Package Manager

## Purpose
Source: https://docs.npmjs.com/getting-started/what-is-npm

Maintain a registry of Node packages. Offers a CLI to install/unistall packages.

## Install
- Requires Node: https://nodejs.org/
- Tutorial: https://github.com/heyallan/node

NPM comes with Node installation, so refer to Node for installtion

## Update
```shell
## update
$ npm cache clean
$ sudo npm install -g npm@latest

## If your npm is broken
$ curl -L https://www.npmjs.org/install.sh | sh
```

## Example
Source: https://docs.npmjs.com/getting-started/installing-npm-packages-locally

Packages can be installed globally to be executed at any location, or locally to be executedonly inside project folder.

Node uses a `package.json` to save detais about what you have installed. NPM will use this file to remember and follow your preferences.

```shell
## create package.json file to save details
$ npm init

## install gulp globally
$ npm install --global gulp

## install gulp in project folder and save details to package.json
$ npm install --save-dev gulp
```

## Reference
https://nodejs.org/api/
