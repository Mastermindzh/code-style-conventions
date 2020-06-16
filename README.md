# mastermindzh' code conventions

In this repo you'll find various code convention guideline files (and some .ignore stuff).
Most of my projects will use at least one of these but I strive to use as many as I can.

**note** these are by no means definitive. Every project has different needs, treat these files as a starting point.

<!-- toc -->

- [repo outline](#repo-outline)
- [@mastermindzh/prettier-config](#mastermindzhprettier-config)
  - [Installation](#installation)
  - [Configuration](#configuration)
    - [package.json](#packagejson)
    - [.prettierrc.js](#prettierrcjs)

<!-- tocstop -->

## repo outline

```js
.
├── prettier // prettier config
│   ├── index.js
│   └── package.json
├── .dockerignore // things to ignore when building dockers
├── .editorconfig // default editor configuration
├── .eslintignore // files to ignore when using eslint
├── .eslintrc // default eslint config
├── .gitignore // files to ignore when working with git
├── LICENSE
└── README.md
```

## @mastermindzh/prettier-config

My preferred prettier configuration.

### Installation

Simply install the package with npm:

`npm install --save-dev @mastermindzh/prettier-config`

### Configuration

Configuring your project to use `@mastermindzh/prettier-config` can be done in several ways.
The easiest is the [package.json](#packagejson) solution, the most extensible is the [.prettierrc.js](#prettierrcjs) version.

#### package.json

Simply add a "prettier" key with the package name:

```json
{
  "prettier": "@mastermindzh/prettier-config"
}
```

#### .prettierrc.js

This solution requires you to put a `.prettierrc.js` file at the root of your project with the following code:

```js
module.exports = {
  ...require("@mastermindzh/prettier-config"),
  // optional overrides:
  jsxBracketSameLine: true,
};
```
