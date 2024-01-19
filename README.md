# Readme

## Setup

How I setup this project?

### First

`git clone -b v3 https://github.com/leokyler/nuxt-starter.git` or download the zip file to get template instead of `npx nuxi@latest init <project-name>
`(It can't run in China!).

### Second

Install the tailwindcss by:

- `npm install --save-dev @nuxtjs/tailwindcss`
- Add @nuxtjs/tailwindcss to the modules section of `nuxt.config.{ts,js}`

```typescript
export default defineNuxtConfig({
  modules: ["@nuxtjs/tailwindcss"],
});
```

### Third

Install and setup test runner that include unit test and e2e test.
How setup?

> https://nuxt.com/docs/getting-started/testing#using-a-nuxt-runtime-environment,
> Maybe update with Time elapsed.

#### Install

- `npm i --save-dev @nuxt/test-utils vitest @vue/test-utils happy-dom playwright-core`,

**Notice,It also installed the e2e modules.**

#### Unit test setup

- Add @nuxt/test-utils/module to your nuxt.config file (optional,and I selected). It adds a Vitest integration to your Nuxt DevTools which supports running your unit tests in development.

```typescript
export default defineNuxtConfig({
  modules: ["@nuxt/test-utils/module"],
});
```

- Create a vitest.config.ts with the following content:

```typescript
import { defineVitestConfig } from "@nuxt/test-utils/config";

export default defineVitestConfig({
  // any custom Vitest config you require
});
```

#### E2E test setup

TBD

## About Test

### Unit test runner

Vitest that the vue project default use.

### E2E test runner

**`@nuxt/test-utils/runtime` and `@nuxt/test-utils/e2e` need to run in different testing environments and so can't be used in the same file.**

TBD

#### Try use cypress / Playwright?

TBD
