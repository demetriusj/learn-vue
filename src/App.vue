<template>
  <div id="app">
    <input autofocus autocomplete="off"
      placeholder="What needs to be done?"
      v-model="newTodoTitle"
      v-on:keyup.enter="addTodo">
    <ul>
      <li v-for="todo in todos">
        <div class="view">
          <label>{{ todo.title }}</label>
          <button @click="deleteTodo(todo)">Delete</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      newTodoTitle: '',
      todos: [
        {title: 'wake up', done: false},
        {title: 'get dressed', done: false},
        {title: 'eat breakfast', done: false},
        {title: 'have a cup of coffee', done: false}
      ]
    }
  },
  methods: {
    addTodo() {
      const title = this.newTodoTitle.trim()
      if (title) {
        this.todos.push({title, done: false})
        this.newTodoTitle = ''
      }
    },
    deleteTodo(todo) {
      this.todos.splice(this.todos.indexOf(todo), 1)
    }
  }
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
