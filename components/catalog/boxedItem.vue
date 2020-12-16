<template>
<div>
    <v-col cols="12">
      <v-card
        shaped
        class="pink-right"
      >
      <router-link
        style="text-decoration: none; color: inherit;"
        :to="category" >
        <v-card-text class="bigger-font">
          {{ category }}
        </v-card-text>
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
  font-size: 125%;
}
</style>