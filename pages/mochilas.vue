<template>
  <v-row>
    <v-col
      v-for="n in 12"
      :key="n"
      class="d-flex child-flex"
      cols="4"
    >
      <v-card>
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
        <v-card-title class="title">
          <v-spacer/>
            Code: XYX-123
          <v-spacer/>
        </v-card-title>
      </v-card>
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
          />
          <v-card-title class="title text-center-align">
            <v-spacer/>
              Code: XYX-123
            <v-spacer/>
          </v-card-title>
      </v-card>
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
        zIndex: 0
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