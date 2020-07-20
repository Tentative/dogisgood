<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 class="main-banner">
      <section id="first">
        <Logo :src="src_home" />
        <Intro />
      </section>

      <section v-show="!isMobile" id="second" :style="style">
        <Service />
      </section>

      <section v-show="!isMobile" id="third">
        <Logo :src="src" />
        <Struttura />
      </section>
      <Cards v-show="isMobile" />
    </v-flex>
    <v-flex xs12 sm8 md6> </v-flex>
  </v-layout>
</template>

<script>
import { Logo, Cards, Intro, Service, Struttura } from '~/components'
export default {
  layout: 'homepage',
  components: {
    Logo,
    Cards,
    Intro,
    Service,
    Struttura
  },
  data() {
    return {
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
