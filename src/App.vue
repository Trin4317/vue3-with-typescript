<script setup lang="ts">
import { reactive, ref } from 'vue'
import JobList from './components/JobList.vue'
import type Job from './types/Job'
import type OrderTerm from './types/OrderTerm'

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
  { title: 'prison guard', location: 'gerudo valley', salary: 32000, id: '5' }
])

const order = ref<OrderTerm>('title')

const handleClick = (term: OrderTerm) => {
  order.value = term
}
</script>

<template>
  <button @click="handleClick('title')">Sort by Title</button>
  <button @click="handleClick('salary')">Sort by Salary</button>
  <button @click="handleClick('location')">Sort by Location</button>
  <JobList :jobs="jobs" :order="order" />
</template>

<style scoped></style>
