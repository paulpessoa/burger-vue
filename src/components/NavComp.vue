<template>
  <v-app-bar
      app
      color="#f2f2f2"
    >


    <router-link to="/">Home</router-link>
    <v-spacer></v-spacer>
    <router-link to="/pedidos">Pedidos</router-link>

    </v-app-bar>
</template>

<script lang="ts">
export default {
    name: 'NavComp'
}
</script>

<style>

</style>