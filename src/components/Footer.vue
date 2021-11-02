<template>
  <v-footer
    dark
    padless
  >
    <v-card
      class="flex"
      flat
      tile
    >
      <v-card-title class="teal">
        <strong class="subheading">Pronto estaremos en servicio!</strong>

        <v-spacer></v-spacer>

        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4"
          dark
          icon
        >
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-title>

      <v-card-text class="py-1 white--text text-center">
        {{ new Date().getFullYear() }} — <strong>Proyecto Cecar</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {

}
</script>

<style>

</style>