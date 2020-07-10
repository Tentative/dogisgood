<template>
  <v-layout id="top" column justify-center align-center>
    <v-flex xs12 class="main-banner">
      <Logo />
      <div id="content-title" class="title text-center">Puppy School</div>
      <div class="text-center">
        <v-sheet id="main-content" color="white"
          >Gli obiettivi di questo percorso sono diversi e contribuiscono tutti
          al benessere di cucciolo e proprietario e alla crescita serena del
          nostro piccolo amico. Nello specifico ci occuperemo di:
          <v-carousel
            cycle
            height="200"
            hide-delimiter-background
            :show-arrows="false"
            style="margin: 20px auto"
          >
            <v-carousel-item v-for="(slide, i) in slides" :key="i">
              <v-sheet :color="colors[i]" height="100%">
                <v-row class="fill-height" align="center" justify="center">
                  <div class="text text-center" style="padding:20px">
                    {{ slide }}
                  </div>
                </v-row>
              </v-sheet>
            </v-carousel-item>
          </v-carousel>
          Questo percorso prevede 6 incontri di un'ora circa, a cadenza
          settimanale, per cuccioli, dai 2 ai 6 mesi, di taglie e razze diverse.
          Nel pacchetto sono compresi anche 3 ingressi da mezza giornata in
          asilo per favorire l'incontro e la socializzazione del cucciolo con
          altri cani in modo del tutto sicuro e protetto sotto la guida dei
          nostri educatori esperti.
        </v-sheet>
        <div id="content-title" class="text-center title">
          Per ulteriori informazioni ed iscrizioni non esitate a<v-btn
            block
            color="#21f37e"
            to="/contact-us"
            >contattarci</v-btn
          >
        </div>

        <div class="media1">
          <v-img :src="struttura1" />
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
</template>

<script>
import Logo from '@/components/Logo.vue'
// import Breadcrumbs from '@/components/Breadcrumbs.vue'
export default {
  name: 'Struttura',
  components: {
    Logo
    // Breadcrumbs
  },

  data() {
    return {
      imgSrc: 'struttura',
      fab: false,
      offsetTop: 0,
      struttura1: require('@/static/struttura3.jpg'),
      struttura2: require('@/static/struttura2.jpg'),
      colors: [
        'indigo',
        'warning',
        'pink darken-2',
        'red lighten-1',
        'deep-purple accent-4'
      ],
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
