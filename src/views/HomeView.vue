<template>
  <div>
    <BannerComp />    
    <h1 class="mt-8">Monte o seu burger</h1>
    <FormBurger/>
  </div>
</template>

<script lang="ts">
import BannerComp from "@/components/BannerComp.vue";
import FormBurger from "@/components/FormBurger.vue";  

  export default {
    name: 'Home',

    components: {
    BannerComp,
    FormBurger
},
  }
</script>
