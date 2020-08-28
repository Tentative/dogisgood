<template>
  <div>
    <v-layout id="top" column justify-center align-center>
      <v-flex xs12 class="main-banner" style="width:100%">
        <!-- <Logo class="hidden-md-and-up" :src="src" /> -->
        <section id="birth" :style="style2" class="hidden-sm-and-down">
          <v-row
            justify="center"
            class="mx-auto"
            style="background-color:rgba(0,0,0,0.4)"
          >
            <v-carousel
              cycle
              height="100vh"
              :hide-delimiters="true"
              width="85vw"
              interval="3000"
            >
              <v-carousel-item
                v-for="(item, i) in items"
                :key="i"
                :src="item.src"
                ><v-col :cols="12" style="background-color:rgba(0,0,0,0.4)">
                  <div class="display-2 text-center text-uppercase white--text">
                    Feste di compleanno
                  </div>
                  <div class="title text-center white--text">
                    Il tuo migliore amico compie gli anni?
                  </div>
                </v-col></v-carousel-item
              >
            </v-carousel>
          </v-row>
        </section>
        <section id="birth" :style="style2" class="hidden-md-and-up">
          <v-row
            justify="center"
            class="mx-auto"
            style="background-color:rgba(0,0,0,0.4)"
          >
            <v-carousel
              cycle
              height="100vh"
              :hide-delimiters="true"
              width="85vw"
            >
              <v-carousel-item
                v-for="(item, i) in items"
                :key="i"
                :src="item.src"
                ><v-col :cols="12" style="background-color:rgba(0,0,0,0.4)">
                  <div class="display-2 text-center text-uppercase white--text">
                    Feste di compleanno
                  </div>
                  <div class="title text-center white--text">
                    Il tuo miglire amico compie gli anni?
                  </div>
                </v-col></v-carousel-item
              >
            </v-carousel>
          </v-row>
        </section>
        <div id="content-title" class="display-1 text-center hidden-md-and-up">
          Festeggia insieme a noi!
        </div>
        <div id="content-title" class=" text-center hidden-sm-and-down">
          Festeggia insieme a noi!
        </div>

        <div class="text-center mx-auto" style="max-width:960px">
          <v-sheet id="main-content" color="white"
            ><div style="margin-bottom:40px">
              <!-- <div
                class="text-center hidden-sm-and-down"
                style="font-size:1.8em"
              >
                Festeggia insieme a noi!
              </div> -->
              <!-- <div
                class="text-center hidden-md-and-up text-uppercase"
                style="font-size:1em"
              >
                Festeggia insieme a noi!<br /><br />
              </div> -->
              <div class="text-left">
                L'Asilo per Cani Dog is Good ti offre una vera festa a quattro
                zampe:
              </div>
            </div>
            <v-card
              color="#42a5f5"
              class="mx-auto"
              max-width="85vw"
              tile
              light
              style="margin:20px"
            >
              <v-card-title class="text-left" style="justify-content:left"
                ><div class="headline text-left">
                  Torta esclusivamente artigianale
                </div></v-card-title
              >
              <v-card-text class="white card-text "
                ><div class="title text-left">
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
              <v-card-title class="text-left" style="justify-content:left"
                ><div class="headline text-left">
                  Animazione dedicata
                </div></v-card-title
              >
              <v-card-text class="white card-text"
                ><div class="title text-left">
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
              <v-card-title class="text-left" style="justify-content:left"
                ><div class="headline text-left">
                  1X foto 20x30cm
                </div></v-card-title
              >
              <v-card-text class="white card-text"
                ><div class="title text-left">
                  Il ricordo con zampa del tuo amico peloso.
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
              <v-card-title class="text-left" style="justify-content:left"
                ><div class="headline text-left">
                  Foto in digitale
                </div></v-card-title
              >
              <v-card-text class="white card-text"
                ><div class="title text-left">
                  Il servizio fotografico di una giornata da non dimenticare.
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
              <v-card-title class="text-left" style="justify-content:left"
                ><div class="headline text-left">
                  Gadget personalizzati
                </div></v-card-title
              >
              <v-card-text class="white card-text"
                ><div class="title text-left">
                  Buonissimi e golosi da regalare agli invitati.
                </div></v-card-text
              ></v-card
            >
            <!-- <div class="media1 hidden-md-and-up" max-width="85vw">
              <v-img :src="compleanno1" />
            </div> -->
          </v-sheet>
          <div id="content-title" class="text-center title">
            Per avere più informazioni
            <p><v-btn color="#21f37e" to="/contattaci">contattaci</v-btn></p>
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
// import Logo from '@/components/Logo.vue'
// import Breadcrumbs from '@/components/Breadcrumbs.vue'
import { FooterLarge } from '@/components/'
export default {
  name: 'Struttura',
  components: {
    // Logo,
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
        ');background-size:cover;background-position:center;width:100%',
      style2:
        'height:100vh;width:100%;background-position:center center;background-size:cover',
      items: [
        {
          src: require('@/static/compleanno-home.jpg')
        },
        {
          src: require('@/static/compleanno-3.JPG')
        },
        {
          src: require('@/static/compleanno-4.JPG')
        },
        {
          src: require('@/static/compleanno-5.JPG')
        },
        {
          src: require('@/static/gallery/compleanni-1.jpg')
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
