<template>
  <div id="app">
    <h1>To-Do list</h1>
    <input type="checkbox" id="todo-item" checked="false" />
    <label for="todo-item">My Todo Item</label>
  </div>
  <div>
    <ul>
      <li>
        <to-do-item label="My Todo Iteml With Label"></to-do-item>
      </li>
    </ul>
  </div>
</template>

<script>
import ToDoItem from "./components/ToDoItem.vue"

export default {
  name: 'app',
  components: {
    ToDoItem
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
