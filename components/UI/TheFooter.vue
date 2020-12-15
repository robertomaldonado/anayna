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
          color="primary"
          fab
          small
          dark
        >
          <v-icon>mdi-facebook</v-icon>
        </v-btn>
      </div>
      <div class="mr-4">
        <v-btn
          color="red"
          fab
          small
          dark
        >
          <v-icon>mdi-instagram</v-icon>
        </v-btn>
      </div>
      <div class="mr-4">
        <v-btn
          color="green"
          fab
          small
          dark
        >
          <v-icon>mdi-whatsapp</v-icon>
        </v-btn>
      </div>
    <v-spacer/>
      <div class="mr-4">
        <v-btn
          color="gray"
          small
          dark
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
      window.open("https://m.facebook.com/anayna.ec");
    }
  }
}
</script>

<style scoped>
</style>
