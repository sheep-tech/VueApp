<template>
  <button @click="count=count*2">Count is: {{count}}</button>

  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App"/>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src

export default defineComponent({
  name: 'Home',
  components: {
    HelloWorld,
  },
  data() {
   return {
    count: 1
   }
  }
  });
</script>
