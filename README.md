# Overview

This repo is just a simple mirror of https://github.com/apache/guacamole-client/tree/master/guacamole-common-js   
Only the js part of the guacamole-client repository is included here to publish it to npmjs

It does automatically download the sources from guacamole's GitHub repo and builds a CommonJS, ES Module and a plain js build.

This package doesn't add or change anything about guacamole-common-js   
It just packages and publishes it, so one can use it easily in a npm project

For more detailed documentation of the API etc. have a look at https://guacamole.apache.org/doc/gug/guacamole-common-js.html

## Setup

```bash
git clone git@github.com:panfiva/guacamole-common-js.git
nvm use current
corepack enable
yarn set version stable
yarn install
```

## Guacamole Update and NPM Publish

```bash
yarn build
npm publish --access public
```

## Usage instructions

Install required modules

```bash
yarn add @panfiva/guacamole-common-js
yarn add @types/guacamole-common-js
```

Create typescript declarations

```js
// guacamole-common-js.d.ts
declare module '@panfiva/guacamole-common-js' {
  export * from '@types/guacamole-common-js'
}
```
