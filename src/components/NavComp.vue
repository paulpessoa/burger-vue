<template>
  <v-app-bar app>

    <router-link to="/">
      <img :src="logo" :alt="alt" id="logo">
    </router-link>

    <v-spacer></v-spacer>
    <router-link to="/profile" v-show="usuarioLogado">
      <v-badge bordered overlap  color="green"
          content="6">
       

        <v-avatar size="40">
          <v-img src="https://cdn.vuetifyjs.com/images/john.png"></v-img>
        </v-avatar>
      </v-badge>
    </router-link>
    <router-link to="/">Home</router-link>
    <router-link to="/pedidos">Pedidos</router-link>
    <router-link v-show="usuarioLogado" to="#">
      <v-btn>Sair</v-btn>
    </router-link>
    <router-link v-show="!usuarioLogado" to="#">
      <v-btn>Login</v-btn>
    </router-link>

  </v-app-bar>
</template>

<script lang="ts">
export default {
  name: 'NavComp',
  props: ["logo", "alt"],
  data() {
    return {
      usuarioLogado: true
    }
  }
}
</script>

<style lang="scss" scoped>
.v-app-bar {
  background-color: #263238 !important;

  img {
    margin: 0 auto;
    width: 50px !important;
    vertical-align: middle;
  }

  a {
    color: #f0f0f0;
    text-decoration: none;
    margin: 12px;
  }
}
</style>