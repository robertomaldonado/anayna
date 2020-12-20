<template>
  <div>
      <v-card shaped style="background-color: #F9C7D6;">
        <v-row justify="center" align="center">
          <v-img
          src="https://storage.googleapis.com/anayna_alpha/main_logo.png"
          max-width="50%"
          />
    </v-row>
       </v-card>
    <v-row justify="center" align="center">
      <div
        v-for="item in includedPages"
        :key="item.id"
      >
        <BoxedItem :category="item.cat" />
      </div>
    </v-row>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'
import BoxedItem from '~/components/catalog/BoxedItem.vue'

export default {
  layout: 'index',
  components: {
    Logo,
    VuetifyLogo,
    BoxedItem
  },
  computed: {
    includedPages () {
      return [
        { id:1, cat:"Lazos"},
        { id:2, cat:"Mochilas"},
        { id:3, cat:"Bolsos"},
        { id:4, cat:"Carteras"},
        { id:5, cat:"MiniMochilas"},
        { id:6, cat:"Monederos"},
        { id:7, cat:"Peluches"},
        { id:8, cat:"Monederos"}
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
  font-size: 120%;
  color:white;
}
</style>
