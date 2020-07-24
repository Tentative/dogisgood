<template>
  <v-layout id="top" column justify-center align-center>
    <v-flex xs12 class="main-banner">
      <Logo />
      <div id="content-title" class="title text-center">
        Contatti
      </div>
      <div class="text-center">
        <v-sheet
          id="main-content"
          color="white"
          class="text-center"
          style="margin-bottom:20px"
        >
          <v-row class="mx-auto" justify="start">
            <v-btn
              class="pa-5"
              tile
              block
              outlined
              color="success"
              href="mailto:info.dogisgood@gmail.com"
            >
              <v-icon size="32px" left>mdi-email</v-icon>
              info.dogisgood@gmail.com
            </v-btn>
          </v-row></v-sheet
        >

        <v-sheet
          id="main-content"
          color="white"
          class="text-center mt-2"
          style="margin-bottom:20px"
        >
          <v-row class="mx-auto" justify="start">
            <v-btn
              class="pa-5"
              tile
              block
              outlined
              color="success"
              href="tel:+393397268386"
            >
              <v-icon size="32px" left>mdi-cellphone</v-icon>
              339-7268386
            </v-btn>
          </v-row></v-sheet
        >
        <v-sheet
          id="main-content"
          color="white"
          class="text-center"
          style="margin-bottom:20px"
        >
          <v-row class="mx-auto" justify="start">
            <v-btn
              class="pa-5"
              tile
              block
              outlined
              color="success"
              href="tel:+3903621821674"
            >
              <v-icon size="32px" left>mdi-deskphone</v-icon>
              0362-1821674
            </v-btn>
          </v-row></v-sheet
        >
      </div>

      <v-sheet
        id="main-content"
        color="white"
        class="text-center"
        style="margin-bottom:20px"
      >
        <Maps />
        Via San Vitale, 129, Seregno (MB)</v-sheet
      >
    </v-flex>
    <v-fab-transition>
      <v-btn
        v-show="fab"
        id="to-top"
        v-scroll="onScroll"
        fixed
        dark
        fab
        bottom
        right
        small
        color="pink"
        @click="$vuetify.goTo('#top', 2500)"
      >
        <v-icon>mdi-chevron-up</v-icon>
      </v-btn>
    </v-fab-transition>
    <!-- <Breadcrumbs :levels="1" /> -->
  </v-layout>
</template>

<script>
import { Logo, Maps } from '@/components'
// import Breadcrumbs from '@/components/Breadcrumbs.vue'
export default {
  name: 'CampoEducazionePrivato',
  components: {
    Logo,
    Maps
    // Breadcrumbs
  },

  data() {
    return {
      imgSrc: 'osteopatia animale',
      mobile: 'tel:+393397268386',
      phone: 'tel:+3903621821674',
      mail: 'mailto:info.dogisgood@gmail.com',
      fab: false,
      offsetTop: 0,
      struttura1: require('@/static/struttura3.jpg'),
      struttura2: require('@/static/struttura2.jpg')
    }
  },
  methods: {
    onScroll(e) {
      if (typeof window === 'undefined') return
      const top = window.pageYOffset || e.target.scrollTop || 0
      this.fab = top > 200
    }
  },
  layout: 'homepage'
}
</script>

<style lang="scss" scoped>
@import '~/assets/content.scss';
</style>
