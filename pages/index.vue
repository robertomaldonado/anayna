<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <div class="text-center">
        <div class="intro allura" />
      </div>
      <v-card>
        <v-card-title class="allura">
          Anayna: Girls' Accessories
        </v-card-title>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    Logo,
    VuetifyLogo
  }
}
</script>

<style>
.intro {
  height: 350px;
  position: relative;
  padding: 30px;
  box-sizing: border-box;
  background-image: url('~assets/images/anayna.png');
  background-position: center;
  background-size: cover;
}
.allura {
  font-family: Allura;
  font-size: 200%;
}
</style>
