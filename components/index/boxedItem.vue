<template>
<div>
    <v-col cols="12">
      <hover>
      <v-card
        shaped 
        outlined
        :elevation="hover ? 10 : 1"
      >
      <router-link
        style="text-decoration: none; color: inherit;"
        :to="category" >
        <v-card-title class="allura">
          <b>{{ category }}</b>
        </v-card-title>
      </router-link>
      </v-card>
      </hover>
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
</style>