<template>
  <v-app>
    <!--Cabeçalho-->
    <NavComp :logo="logo_src" :alt="app_name"/>

    <!--Conteúdo-->
    <v-main>
      <router-view/>
    </v-main>

    <!--Rodapé-->
    <FooterComp/>
  </v-app>
</template>

<script lang="ts">
import Vue from 'vue';
import NavComp from './components/NavComp.vue';
import FooterComp from './components/FooterComp.vue';

export default Vue.extend({
    name: "App",
    data() {
      return {
        logo_src: "/img/logo.png",
        app_name: "Burger Vue"
      }
    },
    components: { 
      NavComp, 
      FooterComp
     }
});
</script>



<style lang="scss">

$primary-color: #263238;
$base-color: #00BFA5;

  *{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }
  *:hover {
    color: $base-color!important;
  }
  h1 {
    text-align: center;
  }

</style>