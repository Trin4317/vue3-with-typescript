<script setup lang="ts">
import { reactive, ref } from "vue";

// using ref()
// const name = ref<string>("Link");
// const age = ref<string | number>(20);

// using reactive()
const state = reactive({
  name: 'Link',
  age: 20 as string | number
})

function changeName(newName: string) {
  state.name = newName
}

function changeAge(newAge: string | number) {
  state.age = newAge
}
</script>

<template>
  <h1>Hello {{ state.name }} - {{ state.age }}</h1>
  <button @click="changeName('Zelda')">Change Name</button>
  <button @click="changeAge(30)">Change Age</button>
</template>

<style scoped>
</style>
