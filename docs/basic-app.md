# Bare-bones Project

Lets remove and clean up the scaffolding code:

```
$ rm -rf src/assets
$ rm -rf src/components
$ rm -rf src/router
```

update `src/App.vue` with:
```
<template>
  <div id="app">
    <h1>Hello World</h1>
  </div>
</template>

<script>
export default {
  name: 'app'
  // data: {},
  // watch: {},
  // computed: {},
  // methods: {},
  // directives: {}
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
```

update `src/main.js` with:
```
import Vue from 'vue'
import App from './App'

/* eslint-disable no-new */
new Vue({
  el: '#app',
  template: '<App/>',
  components: { App }
})
```

### Whats going on here?

index.html includes `src/main.js` and the `new Vue({...})` binds the `<App/>`
component to the `<div id="app"></div>`.

The `components: { App }` is just letting vue template `template: '<App/>'`
know what component code should be used to initialize the `<App/>`

NOTE: The css is using PostCSS

### What does `new Vue({...})` and `App.vue` do

- API details [here](https://vuejs.org/v2/api/#Options-Data)
- How <script/>, <template/> work
- The component is a class

### What are Directives

- [here](https://vuejs.org/v2/api/#Directives)
- how templates do their magic
- {{ }} JS execute

### How to read the docs
