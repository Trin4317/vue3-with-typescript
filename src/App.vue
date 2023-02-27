<script setup lang="ts">
import { reactive, ref } from "vue";
import type Job from "./types/Job";

// using ref()
// const name = ref<string>("Link");
// const age = ref<string | number>(20);

// using reactive()
// const state = reactive({
//   name: 'Link',
//   age: 20 as string | number
// })

// using ref with custom type
const jobs = ref<Job[]>([
  { title: 'farm worker', location: 'lon lon ranch', salary: 30000, id: '1' },
  { title: 'quarryman', location: 'death mountain', salary: 40000, id: '2' },
  { title: 'flute player', location: 'the lost woods', salary: 35000, id: '3' },
  { title: 'fisherman', location: 'lake hylia', salary: 21000, id: '4' },
  { title: 'prison guard', location: 'gerudo valley', salary: 32000, id: '5' },
])
</script>

<template>
  <h1>{{ jobs[0].title }} from {{ jobs[0].location }}</h1>
</template>

<style scoped>
</style>
