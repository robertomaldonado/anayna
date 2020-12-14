<template>
  <v-footer
    :absolute="!fixed"
    app
  >
    <span>&copy; {{ new Date().getFullYear() }}</span>
    <v-spacer/>
    <v-icon class="mr-4">
      mdi-facebook
    </v-icon>
    <v-icon class="mr-4">
      mdi-instagram
    </v-icon>
    <v-icon>
      mdi-whatsapp
    </v-icon>
    <v-spacer/>
    <v-icon>
      mdi-contacts
    </v-icon>
  </v-footer>
</template>

<script>
export default {
}
</script>

<style scoped>
</style>
