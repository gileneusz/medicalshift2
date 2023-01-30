<template>
  <v-container fill-height>
    <v-layout wrap justify-center align-center>
      <!-- <v-card> 
        <v-responsive :aspect-ratio="16/9"> -->
      <v-flex xs12 mb-5>

        <!-- <v-container> -->
        <v-layout justify-center align-center>
          <v-card elevation="5" width="100%">
            <v-responsive :aspect-ratio="16 / 9">

              <iframe width="100%" height="100%" src="https://www.youtube.com/embed/6oJDigZNUqw" frameborder="0"
                allow="encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            </v-responsive>
          </v-card>
        </v-layout>
        <!-- </v-container> -->

      </v-flex>
      <v-flex xs12 mb-5>


        <v-carousel height="auto">
          <v-carousel-item v-for="(item, i) in items" :key="i" :src="item.src" reverse-transition="fade-transition"
            transition="fade-transition"></v-carousel-item>
        </v-carousel>
      </v-flex>

      <!-- </v-responsive>
      </v-card> -->


      <!-- <v-flex md4 hidden-sm-and-down>
        <v-card img="/static/feature1.png" height="250px" />
      </v-flex>
      <v-flex xs12 md8 :pl-5="$vuetify.breakpoint.mdAndUp">
        <h2 class="title mb-3" v-text="$t('Views.Services.heading1')" />
        <p v-text="$t('Views.Services.headingText1')" />
      </v-flex>
      <v-flex xs12 sm8 md6 mb-5 class="py-5">
        <h2 class="title mb-3" v-text="$t('Views.Services.heading2')" />
        <p v-text="$t('Views.Services.headingText2a')" />
        <p v-text="$t('Views.Services.headingText2b')" />
        <p v-text="$t('Views.Services.headingText2c')" />
      </v-flex> -->
      <!--       <v-flex xs12>
        <v-layout justify-center>
          <v-flex xs12 sm10 md8>
            <alpha-testimonial
              :author="testimonial.author"
              :title="testimonial.title"
              :quote="testimonial.quote"
            />
          </v-flex>
        </v-layout>
      </v-flex> -->
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          src: '/static/prototype1.png',
        },
        {
          src: '/static/prototype2.png',
        },
        {
          src: '/static/prototype3.png',
        }
      ],
    }
  },

  metaInfo: {
    title: 'Prototype',
    meta: [
      { name: 'description', content: 'Customized vue-cli templates for Vue and Vuetify' }
    ]
  },
  computed: {
    testimonial() {
      return {
        quote: this.$t('Views.Services.testimonial.quote'),
        author: this.$t('Views.Services.testimonial.author'),
        title: this.$t('Views.Services.testimonial.title')
      }
    }
  }
}
</script>
