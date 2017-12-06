# Editing todo list

Great now its showing up, but how do we make changes to the todo list

```
 export default {
   data() {
     ...
     newTodoTitle: ''
     ...
   }
   ...
   methods: {
     addTodo() {
       const title = this.newTodoTitle && this.newTodoTitle.trim()
       if (title) {
         this.todos.push({title, done: false})
         this.newTodoTitle = ''
       }
     },
     deleteTodo(todo) {
       this.todos.splice(this.todos.indexOf(todo), 1)
     }
   }
   ...
 }
```

```
...
<template>
  <div id="app">
    <input autofocus autocomplete="off"
      placeholder="What needs to be done?"
      v-model="newTodoTitle"
      v-on:keyup.enter="addTodo">
    ...
    <div class="view">
      ...
      <button @click="deleteTodo(todo)">Delete</button>
    </div>
    ...
</template>
```

Now we can add and delete todo items

