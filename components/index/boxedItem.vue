<template>
<div>
    <v-col cols="12">
      <v-card
        shaped 
        outlined
        class="elevation-4"
      >
      <router-link
        style="text-decoration: none; color: inherit;"
        to="/mochilas" >
        <v-card-title class="allura">
          <b>{{ category }}</b>
        </v-card-title>
      </router-link>
      </v-card>
    </v-col>
  </div>
</template>

<script>

export default {
  props:{
    category:{ type:String, default:''}
  },
  components: {
  }
}
</script>

<style>
.category-link {
  height: 100px;
  position: relative;
  padding: 30px;
  box-sizing: border-box;
  background-position: center;
  background-size: cover;
}
.allura {
  font-family: Allura;
  font-size: 200%;
}
a {
  color: black;
  text-decoration: none;
}
.nuxt-link-active {
  color: red;
}
</style>