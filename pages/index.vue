<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 class="main-banner">
      <section id="first">
        <Logo :img-src="imgSrc" />
        <Intro />
      </section>
      <Cards />
    </v-flex>
    <v-flex xs12 sm8 md6> </v-flex>
  </v-layout>
</template>

<script>
import { Logo, Cards, Intro } from '~/components'
export default {
  layout: 'homepage',
  components: {
    Logo,
    Cards,
    Intro
  },
  data() {
    return {
      imgSrc: 'homepage'
    }
  }
}
</script>

<style lang="scss" scoped>
@import '~/assets/homepage.scss';
</style>
