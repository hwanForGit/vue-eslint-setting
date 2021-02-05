<template>
  <!--<div>TodoList</div>-->
  <section>
    <ul>
      <li v-for="(todoItem, index) in todoItems" :key="todoItem">
        {{ todoItem }}
        <button @click="removeTodo(todoItem, index)">삭제</button>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  data() {
    return {
      todoItems: []
    };
  },
  created() {
    if (localStorage.length > 0) {
      for (let i = 0; i < localStorage.length; i++) {
        this.todoItems.push(localStorage.key(i));
      }
    }
  },
  methods: {
    removeTodo(todoItem, index) {
      // 삭제 기능
      // console.log(todoItem, index);
    }
  }
};
</script>

<style></style>
