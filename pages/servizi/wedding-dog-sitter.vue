<template>
  <div>
    <v-layout id="top" column justify-center align-center>
      <v-flex xs12 class="main-banner">
        <!-- <Logo :src="src" class="hidden-md-and-up" /> -->
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
                    Wedding dog sitter
                  </div>
                  <div class="title text-center white--text">
                    Perché rinunciare al tuo migliore amico in uno dei giorni
                    più belli? Con Dog is Good tutto è possibile!
                  </div></v-col
                ></v-carousel-item
              ><v-row justify="center">
                <v-col :cols="6">
                  <v-row justify="center">
                    <div id="wedding" class="title text-left white--text">
                      Ci prenderemo cura di lui per tutta la giornata,
                      assicurandoci che ci sia nei momenti più importanti. Un
                      membro del nostro team a disposizione, un corredino
                      firmato Lussianinda, un reportage della sua giornata...
                      cosa chiedere di più? <br /><br />Averlo al tuo fianco
                      sarà uno dei ricordi più belli!
                    </div>
                  </v-row>
                </v-col>
              </v-row>
            </v-carousel>
          </v-row>
        </section>
        <section id="bautique" :style="style" class="hidden-md-and-up">
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
                    Wedding dog sitter
                  </div>
                  <div class="title text-center white--text">
                    Perché rinunciare al tuo migliore amico in uno dei giorni
                    più belli? Con Dog is Good tutto è possibile!
                  </div></v-col
                ></v-carousel-item
              >
            </v-carousel>
          </v-row>
        </section>
        <div id="content-title" class="title text-center">
          Wedding Dog Sitter
        </div>
        <!-- <div id="content-subtitle" class="subtitle-2 text-center">
          Perché rinunciare al tuo migliore amico in uno dei giorni più belli?
          Con Dog is Good tutto è possibile!
        </div> -->
        <div class="text-center">
          <v-sheet
            id="main-content"
            color="white"
            class="text-left"
            style="margin-bottom:20px;max-width:960px;"
            >Ci prenderemo cura di lui per tutta la giornata, assicurandoci che
            ci sia nei momenti più importanti. Un membro del nostro team a
            disposizione, un corredino firmato Lussianinda, un reportage della
            sua giornata... cosa chiedere di più? <br />Averlo al tuo fianco
            sarà uno dei ricordi più belli!
          </v-sheet>
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
// import { Footer } from '@/components/'
import { FooterLarge } from '@/components/'
export default {
  name: 'Struttura',
  components: {
    // Logo
    // Breadcrumbs
    // Footer
    FooterLarge
  },

  data() {
    return {
      imgSrc: 'struttura',
      fab: false,
      offsetTop: 0,
      src: require('@/static/wedding1.jpg'),
      style:
        'height:100vh;width:100%;background-position:center center;background-size:cover',
      struttura1: require('@/static/struttura3.jpg'),
      struttura2: require('@/static/struttura2.jpg'),
      items: [
        {
          src: require('@/static/wedding1.jpg')
        },
        {
          src: require('@/static/wedding.jpg')
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
      title: 'Dog Is Good | Wedding dog sitter',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content:
            'Perché rinunciare al tuo migliore amico in uno dei giorni più belli? Con Dog is Good tutto è possibile!  Ci prenderemo cura di lui per tutta la giornata, assicurandoci che ci sia nei momenti più importanti.'
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
