<template>
  <v-app>
    <!--Cabeçalho-->
    <NavComp/>

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
    data: () => ({
    //
    }),
    components: { NavComp, FooterComp }
});
</script>
