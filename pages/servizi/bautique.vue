<template>
  <div>
    <v-layout id="top" column justify-center align-center>
      <v-flex xs12 class="main-banner">
        <!-- <Logo :src="items[0].src" class="hidden-sm-and-down" /> -->
        <section id="bautique" :style="style" class="hidden-sm-and-down">
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
                    Bautique
                  </div>
                  <div class="title text-center white--text">
                    Vieni a curiosare nella nostra Bautique! Troverai un sacco
                    di prodotti esclusivi per il tuo cane, ma anche articoli
                    sfiziosi per te!
                  </div></v-col
                ></v-carousel-item
              >
            </v-carousel>
          </v-row>
        </section>
        <div id="content-title" class="display-1 text-center hidden-md-and-up">
          Bautique
        </div>
        <div class="text-left hidden-md-and-up">
          <v-sheet id="main-content" color="white"
            >Vieni a curiosare nella nostra Bautique! Troverai un sacco di
            prodotti esclusivi per il tuo cane, ma anche articoli sfiziosi per
            te!

            <v-carousel
              cycle
              height="200px"
              :hide-delimiters="true"
              width="85vw"
              style="margin-top:20px"
              interval="3000"
            >
              <v-carousel-item
                v-for="(item, i) in items"
                :key="i"
                :src="item.src"
              ></v-carousel-item>
            </v-carousel>
          </v-sheet>
        </div>
        <FooterLarge
          id="to-top"
          v-scroll="onScroll"
          :is_toelettatura="is_toelettatura"
          class="hidden-sm-and-down"
        />
      </v-flex>
      <!-- <v-fab-transition>
        <v-btn
          v-show="fab"
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
  </div>
</template>

<script>
// import Logo from '@/components/Logo.vue'
// import Breadcrumbs from '@/components/Breadcrumbs.vue'
import { FooterLarge } from '@/components/'
export default {
  name: 'Struttura',
  components: {
    // Logo
    // Breadcrumbs
    FooterLarge
  },

  data() {
    return {
      imgSrc: 'struttura',
      fab: false,
      is_toelettatura: true,

      style: 'height:100vh;width:100%;background-position:center center;',
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
  head() {
    return {
      title: 'Dog Is Good | Bautique',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content:
            ' Vieni a curiosare nella nostra Bautique! Troverai un sacco di prodotti esclusivi per il tuo cane, ma anche articoli sfiziosi per te!'
        }
      ]
    }
  },
  layout: 'homepage'
}
</script>

<style lang="scss" scoped>
@import '~/assets/content.scss';
</style>
