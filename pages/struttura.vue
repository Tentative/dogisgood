<template>
  <v-layout id="top" column justify-center align-center>
    <v-flex xs12 class="main-banner">
      <Logo />
      <div id="content-title" class="title text-center">La struttura</div>
      <div class="text-center">
        <v-sheet id="main-content" color="white"
          >La struttura che ospita l’Asilo Dog is Good è stata realizzata per
          rispondere al meglio a tutte le esigenze dei nostri amici pelosi e
          offrire comfort, igiene e sicurezza adeguati al loro benessere. 400 mq
          e un ampio cortile privato a disposizione.
        </v-sheet>
        <Maps />
        <v-row class="hidden-md-and-up">
          <v-col md="6" xs="12">
            <v-carousel
              cycle
              height="400"
              hide-delimiter-background
              :show-arrows="false"
              style="margin: 20px auto"
              class="subheading"
            >
              <v-carousel-item v-for="(carousel, i) in carousels" :key="i">
                <v-sheet height="100%">
                  <v-row class="fill-height" align="center" justify="center">
                    <v-img :src="carousel.src" />
                  </v-row>
                </v-sheet>
              </v-carousel-item>
            </v-carousel>
          </v-col>
        </v-row>
      </div>
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
import { Logo, Maps } from '@/components/'
// import Breadcrumbs from '@/components/Breadcrumbs.vue'
export default {
  name: 'Struttura',
  components: {
    Logo,
    Maps
    // Breadcrumbs
  },

  data() {
    return {
      imgSrc: 'struttura',
      fab: false,
      offsetTop: 0,
      struttura1: require('@/static/struttura3.jpg'),
      struttura2: require('@/static/struttura2.jpg'),
      carousels: [
        {
          src: require('@/static/struttura3.jpg')
        },
        {
          src: require('@/static/struttura-banner-mobile.jpg')
        },
        {
          src: require('@/static/struttura4.jpg')
        },
        {
          src: require('@/static/struttura5.jpg')
        },
        {
          src: require('@/static/struttura6.jpg')
        }
      ]
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
