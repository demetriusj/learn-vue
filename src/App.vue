<template>
  <div id="app">
    <section>
      <header>
        <h1>TODOs</h1>
      </header>
    </section>

    <input autofocus autocomplete="off"
      placeholder="What needs to be done?"
      v-model="newTodoTitle"
      v-on:keyup.enter="addTodo">
    <ul class="todo-list">
      <li v-for="todo in todos">
        <label>{{ todo.title }}</label>
        <button @click="deleteTodo(todo)">Delete</button>
      </li>
    </ul>
    <div v-if="!todos.length">
      <p>Please enter a todo and type "Enter"</p>
    </div>
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
  margin: 60px;
}

input {
  height: 30px;
  width: 100%;
  padding: 0 10px;
}

.todo-list {
  margin: 20px 0 0 0;
  padding: 0;
  list-style: none;
  list-style-type: none !important
}

.todo-list li {
  margin-right: -25px;
  position: relative;
  font-size: 24px;
  border-bottom: 1px solid #ededed;
  display: flex;
  flex-flow: row nowrap;
  flex-direction: row;
  justify-content: space-between;
}

.todo-list li:last-child {
  border-bottom: none;
}

.todo-list li label {
  text-align: left;
  flex-grow: 1;
}
.todo-list li button {
  border: none;
  outline: none;
}

</style>
