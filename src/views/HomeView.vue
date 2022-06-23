<template>
  <div>
    <BannerComp />    
    <h1>Home</h1>
  </div>
</template>

<script lang="ts">
import BannerComp from "@/components/BannerComp.vue";  

  export default {
    name: 'Home',

    components: {
    BannerComp
},
  }
</script>
