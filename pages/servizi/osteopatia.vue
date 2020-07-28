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
                Osteopatia
              </div>
            </v-col>

            <v-row id="main_row" justify="center">
              <v-col :cols="12" style="height:400px"> </v-col>
            </v-row>
            <v-row id="main_row" justify="center"> </v-row>
          </v-container>
        </section>
        <div id="content-title" class=" text-center">Osteopatia Animale</div>
        <div class="text-center">
          <v-sheet id="main-content" color="white" style="max-width:960px"
            ><div>
              L’osteopatia animale è una disciplina olistica complementare alla
              medicina veterinaria, che si avvale di manipolazioni e
              mobilizzazioni terapeutiche, con lo scopo di promuovere il
              benessere psico-fisico dell’animale a 360°. Numerose sono le
              problematiche che possono beneficiare di questo approccio
              (disturbi dell’apparato muscolo-scheletrico, problematiche
              viscerali, riabilitazione post-chirurgica etc.), in quanto riduce
              significativamente il dolore e l’infiammazione, ripristina il
              normale movimento somatico e promuove la capacità di
              autoregolazione interna di ogni organismo, senza l’uso di farmaci.
            </div>
          </v-sheet>
          <div id="content-title" class="title text-center">
            Per info e appuntamenti:
          </div>
          <div class="title text-center" style="margin-bottom:20px">
            Sara Mariani <a href="tel:393490702884">349 0702884</a>
          </div>
        </div>
      </v-flex>
      <!-- <v-fab-transition>
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
      </v-fab-transition> -->
      <!-- <Breadcrumbs :levels="1" /> -->
    </v-layout>
    <FooterLarge class="hidden-sm-and-down" />
  </div>
</template>

<script>
import { Logo, FooterLarge } from '@/components/'
// import Breadcrumbs from '@/components/Breadcrumbs.vue'
export default {
  name: 'Struttura',
  components: {
    Logo,
    FooterLarge
    // Breadcrumbs
  },

  data() {
    return {
      imgSrc: 'osteopatia animale',
      fab: false,
      src: require('@/static/osteopatia-home.jpg'),
      style:
        'background:url(' +
        require('@/static/osteopatia-home.jpg') +
        ');background-position:center center; background-size:cover;width:100%;',
      offsetTop: 0,
      struttura1: require('@/static/struttura3.jpg'),
      struttura2: require('@/static/struttura2.jpg'),
      items: [
        {
          src: require('@/static/bautique-slide-1.jpg')
        },
        {
          src: require('@/static/bautique-slide-2.jpg')
        },
        {
          src: require('@/static/bautique-slide-3.jpg')
        },
        {
          src: require('@/static/bautique-slide-4.jpg')
        },
        {
          src: require('@/static/bautique-slide-5.jpg')
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
