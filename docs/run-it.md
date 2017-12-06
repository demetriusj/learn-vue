# Run it

Lets start the basic vue project now
```
$ npm run dev
```

Lets verify its working
```
$ open http://localhost:8080
$ curl -v http://localhost:8080
```

You can see their is some magic going on, but we can talk about this later.

Lets edit edit `src/components/HelloWorld.vue` and change
```
    return {
      msg: 'Welcome to Your Vue.js App'
    }
```
to
```
    return {
      msg: 'ToDo'
    }
```
and save the file. The application should hot reload at this point.

Great its working!

