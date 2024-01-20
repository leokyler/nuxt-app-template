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

Install and setup test runner that include unit test,component test and e2e test.

About them:

```
当设计你的 Vue 应用的测试策略时，你应该利用以下几种测试类型：

单元测试：检查给定函数、类或组合式函数的输入是否产生预期的输出或副作用。
组件测试：检查你的组件是否正常挂载和渲染、是否可以与之互动，以及表现是否符合预期。这些测试比单元测试导入了更多的代码，更复杂，需要更多时间来执行。
端到端测试：检查跨越多个页面的功能，并对生产构建的 Vue 应用进行实际的网络请求。这些测试通常涉及到建立一个数据库或其他后端。

每种测试类型在你的应用的测试策略中都发挥着作用，保护你免受不同类型的问题的影响。
...

https://cn.vuejs.org/guide/scaling-up/testing.html
```

How setup?

> https://nuxt.com/docs/getting-started/testing#using-a-nuxt-runtime-environment,
> Maybe update with Time elapsed.

#### Install

- `npm i --save-dev @nuxt/test-utils vitest @vue/test-utils happy-dom playwright-core`,

**Notice,It installed the all modules.**

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

#### Component test

TBD

#### E2E test setup

TBD

## About Test

### Unit test & compoment test runner

Vitest that the vue project default use.

### E2E test runner

**`@nuxt/test-utils/runtime` and `@nuxt/test-utils/e2e` need to run in different testing environments and so can't be used in the same file.**

TBD

#### Try use cypress / Playwright/ WebdriverIO?

TBD
