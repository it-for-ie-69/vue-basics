<script setup lang="ts">
import { ref } from "vue";

const data = [
  { id: 1, title: "Todo 1" },
  { id: 2, title: "Todo 2" },
];
const todos = ref(data);
const todoText = ref("");
function handleClick() {
  if (todoText.value === "") return;
  const length = todos.value.length;
  const lastId = todos.value[length - 1].id;
  const newTodo = { id: lastId + 1, title: todoText.value };
  todos.value.push(newTodo);
  todoText.value = "";
}
</script>

<template>
  <h1>Todos</h1>
  <input v-model="todoText" />
  <button @click="handleClick">Add</button>
  <ul>
    <li v-for="(item, index) in todos" :key="item.id">
      {{ item.id }} - {{ item.title }}
    </li>
  </ul>
</template>

<style scoped></style>
