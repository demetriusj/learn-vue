<template>
  <div id="app">
    <ul class="todo-list">
      <li v-for="todo in todos">
        <div class="view">
          <label>{{ todo.title }}</label>
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
      todos: [
        {title: 'wake up', done: false},
        {title: 'get dressed', done: false},
        {title: 'eat breakfast', done: false},
        {title: 'have a cup of coffee', done: false}
      ]
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
