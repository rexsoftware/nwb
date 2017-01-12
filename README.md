# nwb

![Linux](resources/linux.png) [![Travis][travis-badge]][travis]
![Windows](resources/windows.png) [![Appveyor][appveyor-badge]][appveyor]
[![npm package][npm-badge]][npm]
[![Coveralls][coveralls-badge]][coveralls]

nwb provides tooling in a single `devDependency` for:

- [Quick Development with React, Inferno or Preact](#quick-development)
- [React Apps](#react-apps)
- [Preact Apps](#preact-apps)
- [Inferno Apps](#inferno-apps)
- [React Components and Libraries](#react-components-and-libraries)
- [npm Modules for the Web](#npm-modules-for-the-web)

A zero-config development setup is provided, but nwb also supports [configuration](/docs/Configuration.md#configuration) and [plugin modules]((/docs/Plugins.md#plugins)) which add extra functionality (e.g. [Sass](http://sass-lang.com/) support), should you need them

## Install

Installing globally provides an `nwb` command for creating new projects and `react`, `inferno` and `react` commands for quick development:

```
npm install -g nwb
```

To use nwb for build tooling in a project, install it as a `devDependency` and use `nwb` commands in `package.json` `"scripts"`:

```
npm install --save-dev nwb
```

## Quick Development

For quick development with React, Inferno or Preact, use the global `react`, `inferno` or `preact` commands.

```js
import React, {Component} from 'react'

export default class App extends Component {
  render() {
    return <h1>Hello world!</h1>
  }
}
```
```sh
$ react run app.js
✔ Installing react and react-dom
Starting Webpack compilation...
Compiled successfully in 5033 ms.

The app is running at http://localhost:3000/
```
```sh
$ react build app.js
✔ Building React app

File size after gzip:

  dist\app.cff417a3.js  46.72 KB
```

**See [Quick Development with nwb](/docs/guides/QuickDevelopment.md#quick-development-with-nwb) for a more detailed guide.**

## React Apps

Use `nwb new react-app` to create a [React](https://facebook.github.io/react/) app:

```sh
nwb new react-app my-app
cd my-app/
npm start
```

Open [localhost:3000](http://localhost:3000), start editing the code and changes will be hot-reloaded into the running app.

`npm test` will run the app's tests and `npm run build` will create a production build.

**See [Developing React Apps with nwb](/docs/guides/ReactApps.md#developing-react-apps-with-nwb) for a more detailed guide.**

## Preact Apps

Use `nwb new preact-app` to create a [Preact](https://preactjs.com/) app:

```sh
nwb new preact-app my-app
```

Development commands are as above for React apps.

## Inferno Apps

Use `nwb new inferno-app` to create an [Inferno](https://github.com/trueadm/inferno#readme) app:

```sh
nwb new inferno-app my-app
```

Development commands are as above for React apps.

## React Components and Libraries

```sh
nwb new react-component my-component

cd my-component/
```

`npm start` will run a demo app you can use to develop your component or library against.

`npm test` will run the project's tests and `npm run build` will create ES5, ES6 modules and UMD builds for publishing to npm.

**See [Developing React Components and Libraries with nwb](/docs/guides/ReactComponents.md#developing-react-components-and-libraries-with-nwb) for a more detailed guide.**

## npm Modules for the Web

```sh
nwb new web-module my-module

cd my-module/
```

`npm test` will run the project's tests and `npm run build` will create ES5, ES6 modules and UMD builds for publishing to npm.

## [Guides](/docs/guides/#table-of-contents)

- [Quick Development with nwb](/docs/guides/QuickDevelopment.md)
- [Developing React Apps with nwb](/docs/guides/ReactApps.md)
- [Developing React Components and Libraries with nwb](/docs/guides/ReactComponents.md#developing-react-components-and-libraries-with-nwb)
- [Switching to nwb from create-react-app][https://github.com/insin/nwb-from-create-react-app#readme] (as an alternative to ejecting if you need configuration)

## [Documentation](/docs/#table-of-contents)

- [Features](/docs/Features.md#features)
- [Commands](/docs/Commands.md#commands)
  - [`react`](/docs/Commands.md#react)
  - [`nwb`](/docs/Commands.md#nwb)
- [Configuration](/docs/Configuration.md#configuration)
  - [Configuration File](/docs/Configuration.md#configuration-file)
  - [Configuration Object](/docs/Configuration.md#configuration-object)
    - [Babel Configuration](/docs/Configuration.md#babel-configuration)
    - [Webpack Configuration](/docs/Configuration.md#webpack-configuration)
    - [Karma Configuration](/docs/Configuration.md#karma-configuration)
    - [npm Build Configuration](/docs/Configuration.md#npm-build-configuration)
- [Testing](/docs/Testing.md#testing)
- [Plugins](/docs/Plugins.md#plugins)
- [Middleware](/docs/Middleware.md#middleware)
- [Examples](/docs/Examples.md#examples)
- [Frequently Asked Questions](/docs/FAQ.md#frequently-asked-questions)
- [Versioning](/docs/Versioning.md#versioning)

## Why use nwb?

**Get started quickly**. Start developing apps from a single `.js` file or [generate a project skeleton](/docs/Commands.md#new).

**Covers the whole development cycle**. Development tools, testing and production builds for projects work out of the box, no configuration required.

**Flexible**. While everything works out of the box, you can also use an optional [configuration file](/docs/Configuration.md#configuration-file) to tweak things to your liking.

**Manages key development dependencies and configuration for you**. Check out an [example of the effect using nwb had](https://github.com/insin/react-yelp-clone/compare/master...nwb) on the amount of `devDependencies` and configuration to be managed in a real project it was dropped into.

## MIT Licensed

*Operating system icons created with [Icons8](https://icons8.com/)*

[travis-badge]: https://img.shields.io/travis/insin/nwb/master.png?style=flat-square
[travis]: https://travis-ci.org/insin/nwb

[appveyor-badge]: https://img.shields.io/appveyor/ci/insin/nwb/master.png?style=flat-square
[appveyor]: https://ci.appveyor.com/project/insin/nwb

[npm-badge]: https://img.shields.io/npm/v/nwb.png?style=flat-square
[npm]: https://www.npmjs.org/package/nwb

[coveralls-badge]: https://img.shields.io/coveralls/insin/nwb/master.png?style=flat-square
[coveralls]: https://coveralls.io/github/insin/nwb
