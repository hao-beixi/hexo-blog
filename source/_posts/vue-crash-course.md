---
title: vue crash course
date: 2021-10-26 14:57:35
tags:
---
# Links
https://www.youtube.com/watch?v=qZXt1Aom3Cs&t=4955s
# What is Vue?
Vue is a frontend JavaScript framework for building websites & user interfaces

- vue is generally used to create single-page apps that run on the client, but can be used to create full stack applications by making HTTP requests to a backend server. Vue is popular with Node.js & Express(MEVN Stack)
- Vue can also run on the server-side by using a SSR framework like Nuxt

# Why Use Vue?

- create dynamic frontendapps & websites
- Easy learning curve
- Easy to integrate with other projects
- Fast & lightweight
- Virtual DOM
- Extremely popular (and rising)
- Great community

# Basic Layout of a Vue Component
Components include a template for markup, logic including any state/data/methods as well as the styling for that component

You can also pass "props" into a component

```<Header title="Task Tracker" />```

```
<template>
    <header>
        <h1>{{title}}</h1>
    </header>
</template>

<script>
    export default {
        props: {
            title: String,
        },
    }
</script>

<style scoped>
    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
    }
</style>
```

# Working With State / Data
Components can have their own state which can determine how a specific component behaves and what data is displayed

Some state may be local to a specific component and some may be "global" or "app" level state that needs to be shared with multiple components

Vue is a state manager for global statein larger applications

# Vue CLI
Standard tooling for Vue.js development

- Command line interface for creating Vue apps
- Dev server and easy production build
- Optional GUI for managing Vue projects
- Integrated testing, TypeScript support, ESLint & more
```
npm install -g @vue/cli
# OR
yarn global add @vue/cli
```
```
vue  create my-project
# OR
vue ui
```

v3.vuejs.org

https://unpkg.com/vue@next


