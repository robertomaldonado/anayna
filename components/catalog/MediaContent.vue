<template>
  <div>
    <v-row>
    <v-col
      v-for="current_item in item_count" :key="current_item"
      class="d-flex child-flex"
      cols="4" md="3" lg="2" xl="2"
    >
      <ItemDisplay 
        :code="+current_item+1"
        :folder="folder"
        :prefix="prefix"
        @click="showImage(`${current_item+1}`)"
      />
      <v-overlay
        :z-index="zIndex"
        :value="overlay"
      >
        <v-btn
          @click="overlay = false"
        >
          <v-icon>mdi-close-box</v-icon>
          Cerrar
        </v-btn>
        <v-card>
          <v-img
            :src="currentImage"
            max-height="400"
            max-width="400"
            class="grey"
            @click="overlay = false"
          >
          </v-img>
          <v-card-title class="title text-center-align">
            <v-spacer/>
              Code: {{currentCode}}
            <v-spacer/>
          </v-card-title>
        </v-card>
      </v-overlay>
    </v-col>
  </v-row>
  </div>
</template>

<script>
import ItemDisplay from '~/components/UI/ItemDisplay.vue'

export default {
  components: {
    ItemDisplay
  },
  props:{
    item_count: {type:Number, default:0},
    folder: {type:String, default:""},
    prefix: {type:String, default:""}
  },
  data () {
    return {
      currentImage: "",
      currentCode: "",
      overlay: false,
      zIndex: 0
    }
  },
  methods: {
    showImage (item_id) {
      this.currentImage = `https://storage.googleapis.com/anayna_alpha/${this.folder}/${item_id}.jpg`
      this.currentCode = `${this.prefix}-${item_id}`
      this.overlay = !this.overlay
    }
  }
}
</script>

<style>
</style>