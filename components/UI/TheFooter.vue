<template>
  <v-footer
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
          @click="toInstagram()"
          fab
          small
        >
          <v-icon>mdi-instagram</v-icon>
        </v-btn>
      </div>
      <div class="mr-4">
        <v-btn
          @click="openWhatsApp()"
          fab
          small
        >
          <v-icon>mdi-whatsapp</v-icon>
        </v-btn>
      </div>
    <v-spacer/>
      <div class="mr-4">
        <v-btn
          @click="openEmail()"
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
    },
    toInstagram () {
      window.open("https://m.instagram.com/anayna.ec");
    },
    openWhatsApp () {
      window.open("https://api.whatsapp.com/send?phone=+593");
    },
    openEmail () {
      window.open("mailto:replace_me@hotmail.com?subject=Pedidos Anayna&body=Estoy interesado en los items:");
    }
  }
}
</script>

<style scoped>
</style>
