<template>
  <div>
    <v-layout id="top" column justify-center align-center>
      <v-flex xs12 class="main-banner">
        <Logo :src="src" class="hidden-md-and-up" />
        <section id="content_large" class="hidden-sm-and-down" :style="style">
          <v-container style="background-color:rgba(0,0,0,0.4);width:100vw">
            <v-col :cols="12">
              <div
                id="content-title"
                class="  text-center display-4"
                style="color:white"
              >
                Campo di educazione privato
              </div>
            </v-col>

            <v-row id="main_row" justify="center">
              <v-col :cols="12">
                <div class="sub_heading text-center display-3 pa-10">
                  Coming soon
                </div>
              </v-col>
            </v-row>
            <v-row id="main_row" justify="center"> </v-row>
          </v-container>
        </section>
        <section class="hidden-md-and-up">
          <div id="main-content" class="text-center">Coming soon!</div>
        </section>
      </v-flex>

      <!-- <Breadcrumbs :levels="1" /> -->
    </v-layout>
    <FooterLarge class="hidden-sm-and-down" />
  </div>
</template>

<script>
import Logo from '@/components/Logo.vue'
// import Breadcrumbs from '@/components/Breadcrumbs.vue'
import { FooterLarge } from '@/components/'
export default {
  name: 'CampoEducazionePrivato',
  components: {
    Logo,
    // Breadcrumbs
    FooterLarge
  },

  data() {
    return {
      imgSrc: 'osteopatia animale',
      src: require('static/camp2.JPG'),
      fab: false,
      offsetTop: 0,
      struttura1: require('@/static/struttura3.jpg'),
      struttura2: require('@/static/struttura2.jpg'),
      style:
        'background:url(' +
        require('static/camp2.JPG') +
        ');background-size:cover;background-position:center -55px'
    }
  },
  methods: {
    onScroll(e) {
      if (typeof window === 'undefined') return
      const top = window.pageYOffset || e.target.scrollTop || 0
      this.fab = top > 200
    }
  },
  head() {
    return {
      title: 'Dog Is Good | Campo educazione privato',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Coming soon...'
        }
      ]
    }
  },
  layout: 'homepage'
}
</script>

<style lang="scss" scoped>
@import '~/assets/content.scss';
</style>
