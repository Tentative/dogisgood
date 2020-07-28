<template>
  <div>
    <v-layout id="top" column justify-center align-center>
      <v-flex xs12 class="main-banner">
        <Logo class="hidden-md-and-up" :src="src" />
        <section id="content_large" :style="style" class="hidden-sm-and-down">
          <v-container style="background-color:rgba(0,0,0,0.4)">
            <v-row id="main_row" justify="center">
              <v-col :cols="12">
                <div
                  id="content-title"
                  class="  text-center display-4"
                  style="color:white"
                >
                  Feste di compleanno
                </div>
              </v-col>
            </v-row>
            <v-row id="main_row" justify="center">
              <v-col :cols="12">
                <div class="sub_heading text-center display-3 pa-10">
                  Il tuo migliore amico compie gli anni? Festeggia insieme a
                  noi!
                </div>
              </v-col>
            </v-row>
            <v-row id="main_row" justify="center"> </v-row>
          </v-container>
        </section>
        <div id="content-title" class="title text-center hidden-md-and-up">
          Feste di compleanno
        </div>
        <div id="content-title" class=" text-center hidden-sm-and-down">
          L'Asilo per Cani Dog is Good ti offre una vera festa a quattro zampe:
        </div>

        <div class="text-center mx-auto" style="max-width:960px">
          <v-sheet id="main-content" color="white"
            ><div style="margin-bottom:40px">
              Il tuo migliore amico compie gli anni? Festeggia insieme a noi!
              L'Asilo per Cani Dog is Good ti offre una vera festa a quattro
              zampe:
            </div>
            <v-card
              color="#42a5f5"
              class="mx-auto"
              max-width="85vw"
              tile
              light
              style="margin:20px"
            >
              <v-card-title class="text-center "
                ><div class="headline">
                  Torta esclusivamente artigianale
                </div></v-card-title
              >
              <v-card-text class="white card-text "
                ><div class="title">
                  Con ingredienti adatti al tuo cane e ai suoi ospiti.
                </div></v-card-text
              ></v-card
            >
            <v-card
              color="#21f37e"
              class="mx-auto"
              max-width="85vw"
              tile
              light
              style="margin:20px"
            >
              <v-card-title class="text-center"
                ><div class="headline">Animazione dedicata</div></v-card-title
              >
              <v-card-text class="white card-text"
                ><div class="title">
                  Seguita dai nostri esperti educatori cinofili.
                </div></v-card-text
              ></v-card
            >
            <v-card
              color="#42a5f5"
              class="mx-auto"
              max-width="85vw"
              tile
              light
              style="margin:20px"
            >
              <v-card-title class="text-center"
                ><div class="headline">1X foto</div></v-card-title
              >
              <v-card-text class="white card-text"
                ><div class="title">
                  20x30 cm con zampa ricordo del tuo amico peloso.
                </div></v-card-text
              ></v-card
            >
            <v-card
              color="#21f37e"
              class="mx-auto"
              max-width="85vw"
              tile
              light
              style="margin:20px"
            >
              <v-card-title class="text-center"
                ><div class="headline">Foto in digitale</div></v-card-title
              >
              <v-card-text class="white card-text"
                ><div class="title">
                  Del servizio fotografico.
                </div></v-card-text
              ></v-card
            >
            <v-card
              color="#42a5f5"
              class="mx-auto"
              max-width="85vw"
              tile
              light
              style="margin:20px"
            >
              <v-card-title class="text-center"
                ><div class="headline">Gadget</div></v-card-title
              >
              <v-card-text class="white card-text"
                ><div class="title">
                  Buonissimi e golosi personalizzati da regalare agli invitati.
                </div></v-card-text
              ></v-card
            >
            <div class="media1 hidden-md-and-up" max-width="85vw">
              <v-img :src="compleanno1" />
            </div>
          </v-sheet>
          <div id="content-title" class="text-center title">
            Per avere più informazioni
            <p><v-btn color="#21f37e" to="/contact-us">contattaci</v-btn></p>
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
    <FooterLarge class="hidden-sm-and-down" />
  </div>
</template>

<script>
// import Logo from '@/components/Logo.vue'
// import Breadcrumbs from '@/components/Breadcrumbs.vue'
import { FooterLarge, Logo } from '@/components/'
export default {
  name: 'Struttura',
  components: {
    Logo,
    // Footer,
    // Breadcrumbs
    FooterLarge
  },

  data() {
    return {
      imgSrc: 'struttura',
      src: require('@/static/compleanno-home.jpg'),
      fab: false,
      offsetTop: 0,
      compleanno1: require('@/static/compleanno.jpg'),
      style:
        'background:url(' +
        require('@/static/compleanno.jpg') +
        ');background-size:cover;background-position:center'
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
