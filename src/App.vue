<!-- <script setup lang="ts">
const msg = "Hello World";
const num = 1;
const birthYear = 2000;
const currentYear = new Date().getFullYear();
</script>

<template>
  <div>This is just like HTML.</div>
  <div>{{ 1 + 1 }}</div>
  <div>{{ msg }}</div>
  <div>{{ num + 1 }}</div>
  <div>I am {{ currentYear - birthYear }} years old.</div>
</template> -->

<!-- <template>
  <div class="wrapper">
    <h2 class="header">Test CSS</h2>
  </div>
</template>

<style scoped>
.wrapper {
  margin: 0.5em auto;
  width: 95vh;
}
.header {
  color: teal;
}
</style> -->

<!-- <script setup>
function handleClick() {
  alert("Hello!");
}
</script>

<template>
  <button @click="handleClick">Click</button>
</template> -->

<script setup>
let counter = 0;
function handleClick() {
  counter += 1;
  console.log(counter);
}
</script>

<template>
  <div>{{ counter }}</div>
  <button @click="handleClick">Add</button>
</template>
