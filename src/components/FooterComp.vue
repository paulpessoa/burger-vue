<template>
  <v-footer
  >
    <v-card    
      flat
      tile
      class="mx-auto white--text text-center"
    >
      <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4 white--text"
          icon
        >
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text pt-0">
        Phasellus feugiat. Nulla placerat augue montes, nascetur ridiculus mus.
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
       Copyright {{ new Date().getFullYear() }} — <strong>Burger Vue</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script lang="ts">
export default {
    name: 'FooterComp',
    data: () => ({
      icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-linkedin',
        'mdi-instagram',
      ],
    }),
}
</script>

<style>
    .v-footer, .v-card {
        background-color: #263238!important;
    }
</style>