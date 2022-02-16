<template>
  <div>
    <input @change="onFileSelected" type="file" accept="image/png, image/gif, image/jpeg">
  </div>
  
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
    count: 1,
   }
  },
  methods: {
    onFileSelected(event: any) {
      console.log(event)
      const selectedFile = event.target.files[0];
      const formData = new FormData()
      if (selectedFile) {
        formData.append('image', selectedFile, selectedFile.name);
      alert(selectedFile.name)
      // post to backend  server
    }
    
    // onUpload() {
      
    //   }
    }
  }
  });
</script>
