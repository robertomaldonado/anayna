<template>
      <v-card>
      <v-img
        :src="`https://storage.googleapis.com/anayna_alpha/${folder}/${code}.jpg`"
        aspect-ratio="1"
        class="grey lighten-2"
        v-bind="$attrs"
        v-on="$listeners"
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
          {{prefix}}-{{code}}
        </p>
      </v-card>
</template>

<script>
  export default {
    props: {
      code: {type: Number, default: 0},
      prefix: {type: String, default: ''},
      folder: {type: String, default: ''},
      currentImage: {type: String, default: ''}
    },
    data () {
      return {
      }
    },
    methods: {
    }
  }
</script>