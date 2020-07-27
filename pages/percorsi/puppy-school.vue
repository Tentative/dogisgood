<template>
  <div>
    <v-layout id="top" column justify-center align-center>
      <v-flex xs12 class="main-banner">
        <Logo :src="puppy_school" class="hidden-md-and-up" />
        <section id="content_large" :style="style" class="hidden-sm-and-down">
          <v-container style="background-color:rgba(0,0,0,0.6)">
            <v-row id="main_row" justify="center">
              <v-col :cols="12">
                <div
                  id="content-title"
                  class="  text-center display-4"
                  style="color:white"
                >
                  Puppy School
                </div>
              </v-col>
            </v-row>
            <v-row id="main_row" justify="center">
              <v-col :cols="12">
                <div class="sub_heading text-center display-3 pa-10">
                  Gli obiettivi di questo percorso sono diversi e contribuiscono
                  tutti al benessere di cucciolo e proprietario e alla crescita
                  serena del nostro piccolo amico
                </div>
              </v-col>
            </v-row>
            <v-row id="main_row" justify="center"> </v-row>
          </v-container>
        </section>
        <div id="content-title" class="title text-center hidden-sm-and-down">
          Nello specifico ci occuperemo di:
        </div>
        <div id="content-title" class="title text-center hidden-md-and-up">
          Puppy school
        </div>
        <div class="text-center">
          <v-sheet id="main-content" color="white"
            ><div class="hidden-md-and-up">
              Gli obiettivi di questo percorso sono diversi e contribuiscono
              tutti al benessere di cucciolo e proprietario e alla crescita
              serena del nostro piccolo amico. Nello specifico ci occuperemo di:
            </div>
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
                  <v-carousel-item v-for="(slide, i) in slides" :key="i">
                    <v-sheet :color="colors[i]" height="100%">
                      <v-row
                        class="fill-height"
                        align="center"
                        justify="center"
                      >
                        <div class="text text-center" style="padding:20px">
                          {{ slide }}
                        </div>
                      </v-row>
                    </v-sheet>
                  </v-carousel-item>
                </v-carousel>
              </v-col>
            </v-row>
            <v-row style="max-width:960px" class="mx-auto hidden-sm-and-down">
              <v-col :cols="6">
                <v-sheet color="blue" height="100%" dark>
                  <v-row class="fill-height" align="center" justify="center">
                    <div
                      class="text text-center subheading"
                      style="padding:20px"
                    >
                      Guidare il cucciolo nella socializzazione con i propri
                      simili in ambienti diversi, contraddistinti da rumori e
                      odori, per prevenire disturbi del comportamento
                    </div>
                  </v-row>
                </v-sheet>
              </v-col>
              <v-col :cols="6">
                <v-sheet color="#aae56d" height="100%" light>
                  <v-row class="fill-height" align="center" justify="center">
                    <div
                      class="text text-center subheading"
                      style="padding:20px"
                    >
                      Stimolarne le capacità cognitive
                    </div>
                  </v-row>
                </v-sheet>
              </v-col>
              <v-col :cols="4">
                <v-sheet color="blue" height="100%" dark>
                  <v-row class="fill-height" align="center" justify="center">
                    <div
                      class="text text-center subheading"
                      style="padding:20px"
                    >
                      Educare alla relazione con il proprietario affinché sia
                      solida e nutrita di fiducia e rispetto reciproci
                    </div>
                  </v-row>
                </v-sheet>
              </v-col>
              <v-col :cols="4">
                <v-sheet color="#aae56d" height="100%" light>
                  <v-row class="fill-height" align="center" justify="center">
                    <div
                      class="text text-center subheading"
                      style="padding:20px"
                    >
                      Formare il proprietario affinché sia consapevole di tutti
                      i bisogni, psicologici e fisici, del cucciolo
                    </div>
                  </v-row>
                </v-sheet>
              </v-col>
              <v-col :cols="4">
                <v-sheet color="blue" height="100%" dark>
                  <v-row class="fill-height" align="center" justify="center">
                    <div
                      class="text text-center subheading"
                      style="padding:20px"
                    >
                      Formare il cucciolo affinché riconosca, comprenda e
                      rispetti le regole del proprio nucleo famigliare
                    </div>
                  </v-row>
                </v-sheet>
              </v-col>
            </v-row>
            <v-row style="max-width:960px;margin-top:20px" class="mx-auto">
              Questo percorso prevede 6 incontri di un'ora circa, a cadenza
              settimanale, per cuccioli, dai 2 ai 6 mesi, di taglie e razze
              diverse. Nel pacchetto sono compresi anche 3 ingressi da mezza
              giornata in asilo per favorire l'incontro e la socializzazione del
              cucciolo con altri cani in modo del tutto sicuro e protetto sotto
              la guida dei nostri educatori esperti.
            </v-row>
          </v-sheet>
          <div id="content-title" class="text-center title">
            <p>Per ulteriori informazioni ed iscrizioni non esitate a</p>
            <v-btn color="#21f37e" to="/contact-us" style="width:50%;"
              >contattarci</v-btn
            >
          </div>
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
    <FooterLarge />
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
      imgSrc: 'struttura',
      puppy_school: require('@/static/contattaci-banner-mobile.jpg'),
      style:
        'background:url(' +
        require('@/static/contattaci-banner-mobile.jpg') +
        '); background-position: center center; background-size:cover',
      fab: false,
      offsetTop: 0,
      struttura1: require('@/static/struttura3.jpg'),
      struttura2: require('@/static/struttura2.jpg'),
      colors: ['blue', '#aae56d', 'blue', '#aae56d', 'blue'],
      slides: [
        'Guidare il cucciolo nella socializzazione con i propri simili in ambienti diversi, contraddistinti da rumori e odori, per prevenire disturbi del comportamento',
        'Stimolarne le capacità cognitive',
        'Educare alla relazione con il proprietario affinché sia solida e nutrita di fiducia e rispetto reciproci',
        'Formare il proprietario affinché sia consapevole di tutti i bisogni, psicologici e fisici, del cucciolo',
        'Formare il cucciolo affinché riconosca, comprenda e rispetti le regole del proprio nucleo famigliare'
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
