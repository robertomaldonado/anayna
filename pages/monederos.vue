<template>
  <div>
    <v-row>
    <v-col
      v-for="n in 14" :key="n"
      class="d-flex child-flex"
      cols="4" md="3" lg="2" xl="2"
    >
      <ItemDisplay 
        :code="+n"
        folder="monederos"
        prefix="MND"
        @click="showImage(`${n}`)"
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
      this.currentImage = `https://storage.googleapis.com/anayna_alpha/monederos/${item_id}.jpg`
      this.currentCode = `MND-${item_id}`
      this.overlay = !this.overlay
    }
  }
}
</script>

<style>
</style>