<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 class="main-banner">
      <Logo :img-src="imgSrc" />
      <Cards />
    </v-flex>
    <v-flex xs12 sm8 md6> </v-flex>
  </v-layout>
</template>

<script>
import { Logo, Cards } from '~/components'
export default {
  layout: 'homepage',
  components: {
    Logo,
    Cards
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
