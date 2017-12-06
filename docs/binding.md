# Basic Data Binding

Note: Keep in mind the data has to be a function because its Application (think async)!

Add some data for the todo component to render by adding:
```
 export default {
   ...
   data () {
     return {
       todos: [
         {title: 'wake up', done: false},
         {title: 'get dressed', done: false},
         {title: 'eat breakfast', done: false},
         {title: 'have a cup of coffee', done: false}
       ]
     }
   }
   ...
 }
```

Now lets have vue render the todo list by adding:
```
<template>
   <div id="app">
     <ul>
       <li v-for="todo in todos">
         <div>
           <label>{{ todo.title }}</label>
         </div>
       </li>
     </ul>
   </div>
 </template>
 ```
