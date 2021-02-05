<template>
  <div>
    <input v-model="newTodoItem" type="text" />
    <button @click="addTodo">추가</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newTodoItem: ''
    };
  },
  methods: {
    addTodo() {
      // console.log(this.newTodoItem);
      if (this.newTodoItem !== '') {
        const value = this.newTodoItem && this.newTodoItem.trim();
        localStorage.setItem(value, value);
        this.clearInputBox();
      }
    },
    clearInputBox() {
      this.newTodoItem = '';
    }
  }
};
</script>

<style></style>
