
ESLint plugin for React Native
==============================

[![Maintenance Status][status-image]][status-url] [![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![Dependency Status][deps-image]][deps-url] [![Coverage Status][coverage-image]][coverage-url] [![Code Climate][climate-image]][climate-url]

React Native specific linting rules for ESLint. This repository is structured like  (and contains code from) the excellent [eslint-plugin-react](http://github.com/yannickcr/eslint-plugin-react).

# Installation

Install [ESLint](https://www.github.com/eslint/eslint) either locally or globally.

```sh
$ npm install eslint
```

To make most use of this plugin, its recommended to install [eslint-plugin-react](http://github.com/yannickcr/eslint-plugin-react) in addition to [ESLint](https://www.github.com/eslint/eslint). If you installed `ESLint` globally, you have to install eslint-plugin-react globally too. Otherwise, install it locally.

```sh
$ npm install eslint-plugin-react
```

Similarly, install eslint-plugin-react-native


```sh
$ npm install eslint-plugin-react-native
```

# Configuration

Add `plugins` section and specify ESLint-plugin-React (optional) and ESLint-plugin-react-native as a plugin.

```json
{
  "plugins": [
    "react",
    "react-native"
  ]
}
```

If it is not already the case you must also configure `ESLint` to support JSX.

```json
{
  "ecmaFeatures": {
    "jsx": true
  }
}
```

Finally, enable all of the rules that you would like to use.

```json
{
  "rules": {
    "react-native/no-unused-styles": 2,
    "react-native/split-platform-components": 2,
    "react-native/no-inline-styles": 2,
    "react-native/no-color-literals": 2,
  }
}
```

# List of supported rules

* [no-unused-styles](docs/rules/no-unused-styles.md): Detect `StyleSheet` rules which are not used in your React components
* [split-platform-components](docs/rules/split-platform-components.md): Enforce using platform specific filenames when necessary
* [no-inline-styles](docs/rules/no-inline-styles.md): Detect JSX components with inline styles that contain literal values
* [no-color-literals](docs/rules/no-color-literals.md): Detect `StyleSheet` rules and inline styles containing color literals instead of variables

[npm-url]: https://npmjs.org/package/eslint-plugin-react-native
[npm-image]: http://img.shields.io/npm/v/eslint-plugin-react-native.svg?style=flat-square

[travis-url]: https://travis-ci.org/Intellicode/eslint-plugin-react-native
[travis-image]: http://img.shields.io/travis/Intellicode/eslint-plugin-react-native/master.svg?style=flat-square

[deps-url]: https://david-dm.org/Intellicode/eslint-plugin-react-native
[deps-image]: https://img.shields.io/david/dev/Intellicode/eslint-plugin-react-native.svg?style=flat-square

[coverage-url]: https://coveralls.io/r/Intellicode/eslint-plugin-react-native?branch=master
[coverage-image]: http://img.shields.io/coveralls/Intellicode/eslint-plugin-react-native/master.svg?style=flat-square

[climate-url]: https://codeclimate.com/github/Intellicode/eslint-plugin-react-native
[climate-image]: http://img.shields.io/codeclimate/github/Intellicode/eslint-plugin-react-native.svg?style=flat-square

[status-url]: https://github.com/Intellicode/eslint-plugin-react-native/pulse
[status-image]: http://img.shields.io/badge/status-maintained-brightgreen.svg?style=flat-square
