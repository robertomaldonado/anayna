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
        @click="showImage(`${n}`)"
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
        <p class="text-center">
          MLOL-{{n}}
        </p>
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
          <v-card-title class="title text-center-align">
            <v-spacer/>
              Code: {{currentCode}}
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
        currentImage: "",
        currentCode: "",
        overlay: false,
        zIndex: 0
      }
    },
    methods: {
      showImage (item_id) {
        this.currentImage = `https://storage.googleapis.com/anayna_alpha/${item_id}.jpg`
        this.currentCode = `MLOL-${item_id}`
        this.overlay = !this.overlay
      }
    }
  }
</script>