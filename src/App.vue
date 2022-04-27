<template>
  <div id="app">
    <h1>To-Do list</h1>
    <input type="checkbox" id="todo-item" checked="false" />
    <label for="todo-item">My Todo Item</label>
  </div>
  <div>
    <ul>
      <li>
        <to-do-item label="My Todo Iteml With Label" :done="false"></to-do-item>
      </li>
    </ul>
    <ul>
      <li v-for="item in ToDoItems" :key="item.id">
        <to-do-item :label="item.label" :done="item.done" :id="item.id"></to-do-item>
      </li>
    </ul>
  </div>
</template>

<script>

import ToDoItem from "./components/ToDoItem.vue";

import uniqueId from 'lodash.uniqueid';

export default {
  name: "app",
  components: {
    ToDoItem,
  },
  data() {
    return {
      ToDoItems: [
        { id: uniqueId('todo-'), label: "Learn Vue", done: false },
        { id: uniqueId('todo-'), label: "Create a Vue project with the CLI", done: true },
        { id: uniqueId('todo-'), label: "Have fun", done: true },
        { id: uniqueId('todo-'), label: "Create a todo-list", done: false },
      ],
    };
  },
};
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
