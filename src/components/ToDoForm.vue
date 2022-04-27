<template>
  <form @submit.prevent="onsubmit">
    <label for="new-todo-input" @click="label_click"> what needs to be done </label>
    <input type="text" id="new-todo-input" name="new-todo" autocomplete="off" v-model="label"/>
    <button type="submit">Add</button>
  </form>
</template>

<script>
export default {
    methods:{
        label_click(){
            this.label = "clicked!"
        },
        onsubmit(){
            console.log('form submitted, label value ', this.label)
        }
    },
    data() {
        return {
            label:""
        }
    }
};
</script>
