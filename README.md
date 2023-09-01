![repository-banner.png](https://res.cloudinary.com/alvarosaburido/image/upload/v1683452574/repo-banner_d2xeem.png)

# @tresjs/configs 🛠

> Opinionated configuration files Tres Ecosystem. Specifically, this repository contains configuration files for:
> - [ESLint](https://eslint.org/)
> - [TypeScript](https://www.typescriptlang.org/)

- Single quotes, no semi
- Auto fix for formatting (aimed to be used standalone without Prettier)
- Designed to work with TypeScript, Vue out-of-box
- Lint also for json, yaml, markdown
- Sorted imports, dangling commas
- Reasonable defaults, best practices, only one-line of config
- Style principle: Minimal for reading, stable for diff


Based on [@antfu/eslint-config repo](https://github.com/antfu/eslint-config) but modified for Tres Ecosystem.

## Usage

### Install

```
pnpm add -D eslint @tresjs/eslint-config
```

### Configure

Create `.eslintrc.json` in your project root

```json
{
  "extends": "@tresjs/eslint-config"
}

```

## VS Code support (auto fix)

Install VS Code ESLint extension

Add the following settings to your settings.json:

```
{
  "prettier.enable": false,
  "editor.formatOnSave": false,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true,
    "source.organizeImports": false
  },

  // The following is optional.
  // It's better to put under project setting `.vscode/settings.json`
  // to avoid conflicts with working with different eslint configs
  // that does not support all formats.
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    "typescript",
    "typescriptreact",
    "vue",
    "html",
    "markdown",
    "json",
    "jsonc",
    "yaml"
  ]
}
```