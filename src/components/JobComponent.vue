<template>
    <div>
        <ul>
            <li v-for="item in jobs" :key="item.id">{{ item.name }} - {{ item.location }}</li>
        </ul>
    </div>
</template>

<script lang="ts">
import { Job } from '@/model/Job'
import { defineComponent, PropType, ref } from 'vue'

export default defineComponent({
    props: {
        jobs: {
            require: true,
            type: Array as PropType<Job[]>,
        }
    }
})
</script>

<style scoped>
</style>