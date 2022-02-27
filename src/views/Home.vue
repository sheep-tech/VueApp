<template>
  <div>
    <Header />
  </div>

  <JobComponent :jobs="jobs" />
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import JobComponent from '@/components/JobComponent.vue';
import { Job } from '@/model/Job';

export default defineComponent({
  setup() {

    const jobs = ref<Job[]>([
      { id: 1, name: "a", location: "l1" },
      { id: 2, name: "b", location: "l2" },
      { id: 3, name: "c", location: "l3" }
    ])

    return { jobs }

  },
  components: { JobComponent }
});
</script>
