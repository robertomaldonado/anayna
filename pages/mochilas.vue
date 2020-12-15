<template>
  <v-row>
    <v-col
      v-for="n in 12"
      :key="n"
      class="d-flex child-flex"
      cols="3"
    >
      <v-img
        :src="`https://storage.googleapis.com/anayna_alpha/${n}.jpg`"
        aspect-ratio="1"
        class="grey lighten-2"
        @click="showImage(`https://storage.googleapis.com/anayna_alpha/${n}.jpg`)"
      >
        <template v-slot:placeholder>
          <v-row
            class="fill-height ma-0"
            align="center"
            justify="center"
          >
            <v-progress-circular
              indeterminate
              color="grey lighten-5"
            ></v-progress-circular>
          </v-row>
        </template>
      </v-img>
      <v-overlay
      :z-index="zIndex"
      :value="overlay"
      >
      <v-btn
        @click="overlay = false"
      >
        <v-icon>mdi-close-box</v-icon>
      </v-btn>
        <v-img
          :src="currentImage"
          max-height="400"
          max-width="400"
          class="grey"
          @click="overlay = false"
      ></v-img>
      <!-- <v-btn
        class="white--text"
        color="red"
        @click="overlay = false"
      >
        Cerrar Imagen
      </v-btn> -->
      </v-overlay>
    </v-col>
  </v-row>
</template>

<script>
  export default {
    data () {
      return {
        currentImage: "https://storage.googleapis.com/anayna_alpha/1.jpg",
        overlay: false,
        zIndex: 0,
        items: [
          { src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg'},
          { src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg'},
          { src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg'},
          { src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg'},
        ],
      }
    },
    methods: {
      showImage (item) {
        this.currentImage = item
        this.overlay = !this.overlay
      }
    }
  }
</script>