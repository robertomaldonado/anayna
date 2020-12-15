<template>
  <v-footer
    :absolute="!fixed"
    app
  >
    <span>&copy; {{ new Date().getFullYear() }}</span>
    <v-spacer/>
      <div class="mr-4">
        <v-btn
          @click="toFacebook()"
          fab
          small
        >
          <v-icon>mdi-facebook</v-icon>
        </v-btn>
      </div>
      <div class="mr-4">
        <v-btn
          fab
          small
        >
          <v-icon>mdi-instagram</v-icon>
        </v-btn>
      </div>
      <div class="mr-4">
        <v-btn
          fab
          small
        >
          <v-icon>mdi-whatsapp</v-icon>
        </v-btn>
      </div>
    <v-spacer/>
      <div class="mr-4">
        <v-btn
          small
        >
          <v-icon>mdi-contacts</v-icon>
        </v-btn>
      </div>
  </v-footer>
</template>

<script>
export default {
  methods : {
    toFacebook () {
      window.open("https://facebook.com/anayna.ec");
    }
  }
}
</script>

<style scoped>
</style>
