<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 class="main-banner">
      <section id="first">
        <Logo :src="src_home" />
        <Intro />
        <v-btn
          id="to-bottom"
          class="hidden-sm-and-down"
          absolute
          dark
          fab
          bottom
          center
          small
          color="#5ea5ef"
          @click="$vuetify.goTo('#second', options)"
        >
          <v-icon class="pulse">mdi-chevron-down</v-icon>
        </v-btn>
      </section>
      <v-divider class="section_divider_one" color="transparent"></v-divider>

      <section id="second" class="hidden-sm-and-down" :style="style">
        <Service />
        <v-btn
          id="to-third"
          class="hidden-sm-and-down"
          absolute
          dark
          fab
          bottom
          center
          small
          color="#5ea5ef"
          @click="$vuetify.goTo('#third', options)"
        >
          <v-icon class="pulse">mdi-chevron-down</v-icon>
        </v-btn>
      </section>

      <section id="third" class="hidden-sm-and-down">
        <v-divider class="section_divider_two" color="transparent"></v-divider>
        <Logo :src="src" />
        <Struttura />
        <v-btn
          id="to-bottom"
          class="hidden-sm-and-down"
          absolute
          dark
          fab
          bottom
          center
          small
          color="#5ea5ef"
          @click="$vuetify.goTo('#fourth', options)"
        >
          <v-icon class="pulse">mdi-chevron-down</v-icon>
        </v-btn>
      </section>

      <section id="fourth" class="hidden-sm-and-down">
        <v-divider class="section_divider_one" color="transparent"></v-divider>
        <no-ssr>
          <video-background
            :src="src_video"
            style="height: 100vh;"
            overlay="linear-gradient(45deg,rgba(0,0,0,.2),rgba(0,0,0.2))"
          >
            <End />
          </video-background>
        </no-ssr>
        <!-- <v-btn
          v-show="!isMobile"
          id="to-top"
          absolute
          dark
          fab
          bottom
          center
          small
          color="#5ea5ef"
          @click="$vuetify.goTo('#first', options)"
        >
          <v-icon class="pulse">mdi-chevron-up</v-icon>
        </v-btn> -->
      </section>
      <Cards class="hidden-md-and-up" />
    </v-flex>
    <v-flex xs12 sm8 md6> </v-flex>
  </v-layout>
</template>

<script>
// import VideoBackground from 'vue-responsive-video-background-player'
import { Logo, Cards, Intro, Service, Struttura, End } from '~/components'
export default {
  layout: 'homepage',
  components: {
    Logo,
    Cards,
    Intro,
    Service,
    Struttura,
    End
    // VideoBackground
  },
  data() {
    return {
      VideoBackground: null,
      src_video: require('@/static/cagnociao.mp4'),
      imgSrc: 'homepage',
      src_home: require('@/static/index-banner-mobile.jpg'),
      src: require('@/static/struttura-alt.jpg'),
      imgSrc_struttura: 'struttura',
      style:
        "background:url('" + require('@/static/sfondo-servizi.jpg') + "');",
      style_servizi:
        "background:url('" + require('@/static/struttura-desktop.jpg') + "');",
      to_second: '$vuetify.goTo("#second", 2500)',

      duration: 500,
      offset: -64
    }
  },
  computed: {
    // isMobile() {
    //   return !(window.innerWidth > 768)
    // },
    options() {
      return {
        duration: this.duration,
        offset: this.offset
        // easing: this.easing
      }
    }
  },
  mounted() {
    this.VideoBackground = require('~/plugins/vue-video-background.client.js')
  },
  methods: {}
}
</script>

<style lang="scss" scoped>
@import '~/assets/homepage.scss';
</style>
