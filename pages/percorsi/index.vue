<template>
  <div>
    <v-layout id="top" column justify-center align-center>
      <v-flex xs12 class="main-banner">
        <Logo :src="percorsi1" class="hidden-md-and-up" />
        <section id="content_large" :style="style" class="hidden-sm-and-down">
          <v-container style="background-color:rgba(0,0,0,0.6)">
            <v-row id="main_row" justify="center">
              <v-col :cols="12">
                <div
                  id="content-title"
                  class="  text-center display-4"
                  style="color:white"
                >
                  Percorsi educativi
                </div>
              </v-col>
            </v-row>
            <v-row id="main_row" justify="center">
              <v-col :cols="12">
                <div class="sub_heading text-center display-3 pa-10">
                  Il nostro è il metodo di educazione detto gentile, adatto a
                  qualunque cane.
                </div>
              </v-col>
            </v-row>
            <v-row id="main_row" justify="center"> </v-row>
          </v-container>
        </section>
        <section id="content_description">
          <v-row align="start" class="mx-auto">
            <v-row style="width:100%">
              <div id="content-title" class="display-2 text-center">
                Educazione
              </div>
            </v-row>
            <v-col :cols="12" md="6" xs="12">
              <div class="text-center">
                <v-sheet id="main-content" color="#aae56d"
                  >Il nostro è il metodo di educazione detto gentile, adatto a
                  qualunque cane, indipendentemente da razza, età, sesso e
                  caratteristiche individuali, e personalizzato con uno studio
                  attento dell’animale affinché possa offrire la massima
                  efficacia. Durante un percorso di educazione, cane e
                  proprietario imparano, insieme, gli esercizi di base utili
                  nella vita quotidiana, come la condotta al guinzaglio e il
                  richiamo, ma soprattutto a relazionarsi nel migliore dei modi,
                  a risolvere piccoli e grandi problemi ed avere così una vita
                  insieme più felice e semplice per entrambi.
                </v-sheet>
              </div>
            </v-col>
            <v-col :cols="12" xs="12" md="6" style="height:100%">
              <v-card
                class="mx-auto"
                color="#26c6da"
                width="85vw"
                dark
                max-width="100%"
                height="100%"
              >
                <v-card-title>
                  <v-icon large left>
                    mdi-paw
                  </v-icon>
                  <span class="title font-weight-light">Puppy School</span>
                </v-card-title>

                <v-card-text class="headline font-weight-bold">
                  Gli obiettivi di questo percorso sono diversi e contribuiscono
                  tutti al benessere di cucciolo e proprietario e alla crescita
                  serena del nostro piccolo amico.
                </v-card-text>

                <v-card-actions>
                  <v-list-item class="grow">
                    <v-list-item-avatar color="grey darken-3">
                      <v-img class="elevation-6" :src="logoSrc"></v-img>
                    </v-list-item-avatar>

                    <v-list-item-content>
                      <v-list-item-title>Dog Is Good</v-list-item-title>
                    </v-list-item-content>

                    <v-row align="center" justify="end">
                      <v-btn
                        outlined
                        color="purple"
                        text
                        to="./percorsi/puppy-school"
                      >
                        Scopri
                      </v-btn>
                    </v-row>
                  </v-list-item>
                </v-card-actions>
              </v-card>
              <v-card
                color="#26c6da"
                dark
                style="margin-top:20px"
                width="85vw"
                class="mx-auto"
              >
                <v-card-subtitle class="headline font-weight-bold"
                  >Se invece sei alla ricerca del tuo amico peloso, ti offriamo
                  la migliore consulenza, competente e attenta, che ti guidi in
                  un percorso di adozione maturo e
                  responsabile..</v-card-subtitle
                >
              </v-card>
            </v-col>
          </v-row>
        </section>
        <Prezzi />
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
    <FooterLarge />
  </div>
</template>

<script>
import { Logo, Prezzi, FooterLarge } from '@/components/'
// import Breadcrumbs from '@/components/Breadcrumbs.vue'
export default {
  name: 'Percorsi',
  components: {
    Logo,
    Prezzi,
    FooterLarge
    // Breadcrumbs
  },

  data() {
    return {
      imgSrc: this.$route.name,
      style:
        'background:url(' +
        require('@/static/struttura2.jpg') +
        ');background-position:center ;background-size:cover',
      fab: false,
      offsetTop: 0,
      percorsi1: require('@/static/struttura2.jpg'),
      logoSrc: require('@/static/logo.jpg')
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

<style lang="scss">
@import '~/assets/content.scss';
</style>
