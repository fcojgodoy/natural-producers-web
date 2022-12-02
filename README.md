# Nuxt 3 Minimal Starter

Look at the [Nuxt 3 documentation](https://nuxt.com/docs/getting-started/introduction) to learn more.

## Prerequisites

[Prerequisites](https://nuxt.com/docs/getting-started/installation#prerequisites).

## Setup

Make sure to install the dependencies:

```
pnpm install --shamefully-hoist
```

## Postrequisites

In VSCode, [enable Volar Takeover Mode](https://nuxt.com/docs/getting-started/installation#prerequisites).

In `nuxt.config.ts`, [disable generating the shim for \*.vue files](https://nuxt.com/docs/getting-started/installation#prerequisites).

## ESLint configuration

### ESLint init

Need Typescript:

```
pnpm i -D typescript
```

Then init and config ESLint with this config:

```
pnpm create @eslint/config
```

✔ How would you like to use ESLint? · problems

✔ What type of modules does your project use? · esm

✔ Which framework does your project use? · vue

✔ Does your project use TypeScript? · No / Yes

✔ Where does your code run? · browser, node

✔ What format do you want your config file to be in? · JavaScript

This automatily install and create basic configuration for:

- [ESLint](https://eslint.org/)

- [eslint-plugin-vue](https://eslint.vuejs.org/)

- [typescript-eslint](https://typescript-eslint.io/)

### plugin:vue/vue3-recommended

La configuración automática de ESLint añade la bundle configuration `plugin:vue/vue3-essential`.
Cambiar por `plugin:vue/vue3-recommended`.

These are stricter rules.
More info in https://eslint.vuejs.org/user-guide/#bundle-configurations

### eslint-plugin-nuxt

ESLint plugin for Nuxt.js

Homepage: https://github.com/nuxt/eslint-plugin-nuxt#readme

```
pnpm i -D eslint-plugin-nuxt
```

```
{
  "extends": [
    "plugin:nuxt/recommended"
  ]
}
```

### warning Use the latest vue-eslint-parser

La configuración automática de ESLint crea un error:

```
warning  Use the latest vue-eslint-parser
```

See https://eslint.vuejs.org/user-guide/#what-is-the-use-the-latest-vue-eslint-parser-error

### root: true

Añadir la opción:

```
root: true
```

See https://eslint.org/docs/latest/user-guide/configuring/configuration-files#cascading-and-hierarchy

### Notes

In this [article](https://itnext.io/nuxt-3-first-steps-c23d142405c4) is recommended use [@vue/eslint-config-standard]. I don't sure if this is a good idea. Further, if we use Typescript, maybe we should use [@vue/eslint-config-standard-with-typescript]. And in both cases alongside [@rushstack/eslint-patch]. See https://github.com/vuejs/eslint-config-standard.

### Add linter script on papckage.json

```
"lint": "eslint --ext .ts,.vue ."
```

## Prettier configuration

Follow install guide: https://prettier.io/docs/en/install.html

## Integrate Prettier with linters

Follow instructions on: https://prettier.io/docs/en/integrating-with-linters.html

## Commit Message Guidelines

Follow [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)

## Development Server

Start the development server on http://localhost:3000

```bash
pnpm dev
```

## Production

Build the application for production:

```bash
pnpm build
```

Locally preview production build:

```bash
pnpm preview
```

Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.
