# Setup scaffolding for todo app

Lets use Vuejs CLI to do this for us.

- Full doc can be found [here](https://vuejs.org/v2/guide/installation.html)
- Has helpful features that support all aspects of the development cycle
- It's opinionated but flexible
- Their are better scaffolding for vuejs i.e. nuxt

`NOTE: In the real world most companies will not use the CLI,
but have a custom in-house build chain.`

```
install "Vue.js devtools" chrome plugin from chrome store
```

```
install vue-cli
$ npm install --g vue-cli

create a new project using the "webpack" template
$ vue init webpack todo-app

when prompted please pick:
? Project name todo-app
? Project description My first Vue project
? Author [You]
? Vue build standalone
? Install vue-router? Yes
? Use ESLint to lint your code? Yes
? Pick an ESLint preset Standard
? Setup unit tests No
? Setup e2e tests with Nightwatch? No

$ cd todo-app
$ npm install
```

Lets look around and try to understand what the cli created.
More documentation [here](https://nuxtjs.org/guide/directory-structure)

```
index.html
src/*
```
