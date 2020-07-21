<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 class="main-banner">
      <section id="first">
        <Logo :src="src_home" />
        <Intro />
      </section>
      <v-divider class="section_divider_one" color="transparent"></v-divider>

      <section v-show="!isMobile" id="second" :style="style">
        <Service />
      </section>

      <section v-show="!isMobile" id="third">
        <v-divider class="section_divider_two" color="transparent"></v-divider>
        <Logo :src="src" />
        <Struttura />
      </section>

      <section v-show="!isMobile" id="fourth">
        <v-divider class="section_divider_one" color="transparent"></v-divider>
        <video-background
          :src="src_video"
          style="height: 100vh;"
          overlay="linear-gradient(45deg,rgba(0,0,0,.2),rgba(0,0,0.2))"
        >
          <End />
        </video-background>
      </section>
      <Cards v-show="isMobile" />
    </v-flex>
    <v-flex xs12 sm8 md6> </v-flex>
  </v-layout>
</template>

<script>
import VideoBackground from 'vue-responsive-video-background-player'
import { Logo, Cards, Intro, Service, Struttura, End } from '~/components'
export default {
  layout: 'homepage',
  components: {
    Logo,
    Cards,
    Intro,
    Service,
    Struttura,
    End,
    VideoBackground
  },
  data() {
    return {
      src_video: require('@/static/cagnociao.mp4'),
      imgSrc: 'homepage',
      src_home: require('@/static/index-banner-mobile.jpg'),
      src: require('@/static/struttura-desktop.jpg'),
      imgSrc_struttura: 'struttura',
      style:
        "background:url('" + require('@/static/sfondo-servizi.jpg') + "');",
      style_servizi:
        "background:url('" + require('@/static/struttura-desktop.jpg') + "');"
    }
  },
  computed: {
    isMobile() {
      return !(window.innerWidth > 768)
    }
  }
}
</script>

<style lang="scss" scoped>
@import '~/assets/homepage.scss';
</style>
