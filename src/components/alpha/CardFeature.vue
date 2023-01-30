<template>
  <v-container grid-list-xl pa-0>
    <v-layout row wrap justify-center>
      <v-flex xs12 sm6 md4 d-flex v-for="(feature, i) in features" :key="i">

        <v-card elevation="5" tile>
          <!-- <iframe :height="cardHeight" src="https://www.youtube.com/embed/6oJDigZNUqw"  frameborder="0" allow="encrypted-media; gyroscope; picture-in-picture"  allowfullscreen></iframe>    -->
          <!-- <iframe :height="cardHeight" src="https://www.youtube.com/embed/6oJDigZNUqw" width="640" height="360" frameborder="0" allow="encrypted-media; gyroscope; picture-in-picture"  allowfullscreen></iframe>  -->

          <v-img :src="`/static/${feature.img}.png`" :height="cardHeight" />
          




          <v-card-title class="title" v-text="feature.title" />
          <v-card-text v-text="feature.text" />
        </v-card>
      </v-flex>
    </v-layout>
    <v-dialog v-model="dialog">
      
            <v-layout row wrap justify-center>
              <v-flex xs12 sm6 md4>


                <v-card>
                  <iframe width="640" height="360" src="https://www.youtube.com/embed/6oJDigZNUqw" frameborder="0"
                    allow="encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                  <v-card-title class="text-h5 grey lighten-2">
                    Privacy Policy
                  </v-card-title>

                  <v-card-text>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore
                    et
                    dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
                    aliquip
                    ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum
                    dolore eu
                    fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia
                    deserunt mollit anim id est laborum.
                  </v-card-text>

                </v-card>
              </v-flex>
            </v-layout>
          </v-dialog>
  </v-container>
</template>

<script>
export default {

  data() {
    return {
      dialog: false,
    }
  },
  name: 'alpha-card-feature',

  props: {
    cardHeight: {
      type: String,
      default: '200px'
    },
    features: {
      type: Array,
      default: () => ([])
    }
  }
}
</script>
