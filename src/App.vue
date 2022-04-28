<template>
	<div id="app">
		<img width="5%" src="./assets/logo.png" />
		<HelloWorld />
		<BootstrapPagination />
	</div>
</template>

<script>
import HelloWorld from "./components/HelloWorld"
import BootstrapPagination from "./components/BootstrapPagination"

// import ToDoItem from "./components/ToDoItem.vue"
// import uniqueId from "lodash.uniqueid"
// import ToDoForm from "./components/ToDoForm.vue"
// import TabSearch from "./components/TabSearch.vue"
//import "./assets/reset.css"

export default {
	name: "app",
	components: {
		HelloWorld,
		BootstrapPagination,
		// ToDoItem,
		// ToDoForm,
		// TabSearch
	},
	data() {
		return {
			name: "BootstrapVue",
			show: true,
			// ToDoItems: [
			// 	{ id: uniqueId("todo-"), label: "Learn Vue", done: false },
			// 	{
			// 		id: uniqueId("todo-"),
			// 		label: "Create a Vue project with the CLI",
			// 		done: true,
			// 	},
			// 	{ id: uniqueId("todo-"), label: "Have fun", done: true },
			// 	{
			// 		id: uniqueId("todo-"),
			// 		label: "Create a todo-list",
			// 		done: false,
			// 	},
			// ],
		}
	},
	methods: {
		addTodo(toDoLabel) {
			console.log("To-do added with label : ", toDoLabel)
			// this.ToDoItems.push({
			// 	id: uniqueId("todo-"),
			// 	label: toDoLabel,
			// 	done: false,
			// })
		},
		updateDoneStatus(toDoId) {
			const toDoToUpdate = this.ToDoItems.find(
				(item) => item.id === toDoId
			)
			toDoToUpdate.done = !toDoToUpdate.done
		},
		deleteToDo(toDoId) {
			const itemIndex = this.ToDoItems.findIndex(
				(item) => item.id === toDoId
			)
			this.ToDoItems.splice(itemIndex, 1)
			this.$refs.listSummary.focus()
		},
		editToDo(toDoId, newLabel) {
			console.log("edit to do")
			const toDoToEdit = this.ToDoItems.find((item) => item.id === toDoId)
			toDoToEdit.label = newLabel
		},
	},
	computed: {
		listSummary() {
			const numberFinishedItems = this.ToDoItems.filter(
				(item) => item.done
			).length
			return `${numberFinishedItems} out of ${this.ToDoItems.length} items completed`
		},
	},
}
</script>

<style>
#app {
	font-family: Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #000;
	margin-top: 10px;
}
</style>
