<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 class="main-banner">
      <section id="first">
        <Logo :img-src="imgSrc" />
        <Intro />
      </section>

      <section id="second">
        <Service v-show="!isMobile" />
      </section>

      <Cards v-show="isMobile" />
    </v-flex>
    <v-flex xs12 sm8 md6> </v-flex>
  </v-layout>
</template>

<script>
import { Logo, Cards, Intro, Service } from '~/components'
export default {
  layout: 'homepage',
  components: {
    Logo,
    Cards,
    Intro,
    Service
  },
  data() {
    return {
      imgSrc: 'homepage'
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
