<script setup lang="ts">
import type { PropType } from "vue";
import type Job from "@/types/Job";

// receive props from parent
defineProps({
    jobs: {
        required: true,
        type: Array as PropType<Job[]>
    }
})
</script>

<template>
    <div class="job-list">
        <ul>
            <li v-for="job in jobs" :key="job.id">
                <h2>{{ job.title }} in {{ job.location }}</h2>
                <div class="salary">
                    <p>{{ job.salary }} rupees</p>
                </div>
                <div class="description">
                    <p>Lorem ipsum.</p>
                </div>
            </li>
        </ul>
    </div>
</template>

<style scoped>

</style>