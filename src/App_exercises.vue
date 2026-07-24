<!-- ####################################### -->
<!-- Exercise 1: Template Syntax -->
<!-- ####################################### -->
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

<!-- ####################################### -->
<!-- Exercise 2: Styles -->
<!-- ####################################### -->
<!-- <template>
  <div class="wrapper">
    <h2 class="header">Test CSS</h2>
  </div>
</template>

<style scoped>
.wrapper {
  background-color: lightgray;
}
.header {
  color: teal;
}
</style> -->

<!-- ####################################### -->
<!-- Exercise 3: Event Handling -->
<!-- ####################################### -->
<!-- <script setup lang="ts">
function handleClick() {
  alert("Hello!");
}
</script>

<template>
  <button @click="handleClick">Click</button>
</template> -->

<!-- ####################################### -->
<!-- Exercise 4: Component -->
<!-- ####################################### -->
<!-- <script setup lang="ts">
import NavBar from "./Navbar.vue";
</script>

<template>
  <NavBar />
  <h1>Welcome to My App</h1>
</template> -->

<!-- ####################################### -->
<!-- Exercise 5: State (not working)-->
<!-- ####################################### -->
<!-- <script setup>
let counter = 0;
function handleClick() {
  counter += 1;
  console.log(counter);
}
</script>

<template>
  <div>{{ counter }}</div>
  <button @click="handleClick">Add</button>
</template> -->

<!-- ####################################### -->
<!-- Exercise 6: State (Working)-->
<!-- ####################################### -->
<!-- <script setup lang="ts">
import { ref } from "vue";

const counter = ref(0);

function handleClick() {
  counter.value += 1;
}
</script>

<template>
  <div>{{ counter }}</div>
  <button @click="handleClick">Add</button>
</template> -->

<!-- ####################################### -->
<!-- Exercise 7: Form 1 -->
<!-- ####################################### -->
<!-- <script setup lang="ts">
import { ref } from "vue";

const name = ref("");
function handleInput(e) {
  name.value = e.target.value;
}

function handleClick() {
  name.value = "";
}
</script>

<template>
  <input @input="handleInput" :value="name" placeholder="Type your name" />
  <p>Hello, {{ name }}</p>
  <button @click="handleClick">Submit</button>
</template> -->

<!-- ####################################### -->
<!-- Exercise 7: Form 2 -->
<!-- ####################################### -->
<!-- <script setup lang="ts">
import { ref } from "vue";

const name = ref("");
function handleClick() {
  name.value = "";
}
</script>

<template>
  <input v-model="name" placeholder="Type your name" />
  <p>Hello, {{ name }}</p>
  <button @click="handleClick">Submit</button>
</template> -->

<!-- ####################################### -->
<!-- Exercise 8: List Rendering -->
<!-- ####################################### -->

<!-- <script setup lang="ts">
import { ref } from "vue";
const items = ref(["Item 1", "Item 2", "Item 3"]);
</script>

<template>
  <ul>
    <li v-for="(item, index) in items" :key="index">
      {{ index + 1 }} - {{ item }}
    </li>
  </ul>
</template> -->

<!-- ####################################### -->
<!-- Exercise 9: Conditional Rendering -->
<!-- ####################################### -->
<script setup lang="ts">
import { ref } from "vue";
const toggle = ref(true);

function handleClick() {
  toggle.value = !toggle.value;
}
</script>

<template>
  <button @click="handleClick">Toggle</button>
  <div v-if="toggle">
    <p>Hello, World!</p>
  </div>
  <div v-else>
    <p>Goodbye, World!</p>
  </div>
</template>
