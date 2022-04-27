<template>
  <form @submit.prevent="onsubmit">
    <h2 class="label-wrapper">
      <label for="new-todo-input" class="label__lg" @click="label_click">
        What needs to be done?
      </label>
    </h2>
    <input
      type="text"
      id="new-todo-input"
      name="new-todo"
      autocomplete="off"
      v-model.lazy.trim="label"
      class="input__lg"
    />
    <button type="submit" class="btn btn__primary btn__lg">Add</button>
  </form>
</template>

<script>
export default {
  methods: {
    label_click() {
      this.label = "clicked!";
    },
    onsubmit() {
      if (this.label === "") {
        return;
      }
      // console.log('form submitted, label value ', this.label)
      this.$emit("todo-added", this.label);
      this.label = "";
    },
  },
  data() {
    return {
      label: "",
    };
  }
};
</script>
