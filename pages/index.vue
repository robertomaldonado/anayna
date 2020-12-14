<template>
<div>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <div class="text-center">
        <div class="intro allura" />
      </div>
      <v-card 
        class="elevated-5"
      >
        <v-card-text class="bigger-font">
            Revisa nuestro catálogo
        </v-card-text>
      </v-card>
    </v-col>
    </v-row>
    <v-row justify="center" align="center">
    <div
      v-for="item in includedPages"
      :key="item.id"
    >
    <BoxedItem
      :category="item.cat"
    />
    </div>
    </v-row>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  layout: 'index',
  components: {
    Logo,
    VuetifyLogo
  },
  computed: {
    includedPages () {
      return [
        {
          id:1,
          cat:"Lazos"
        },
        {
          id:2,
          cat:"Mochilas"
        },
        {
          id:3,
          cat:"Llaveros"
        },
        {
          id:4,
          cat:"Monederos"
        },
        {
          id:5,
          cat:"Peluches"
        }
      ]
    }
  }
}
</script>

<style>
.intro {
  height: 300px;
  position: relative;
  padding: 30px;
  box-sizing: border-box;
  background-image: url('~assets/images/anayna.png');
  background-position: center;
  background-size: cover;
}
.bigger-font {
  font-size: 150%;
}
</style>
