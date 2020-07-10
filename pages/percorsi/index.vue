<template>
  <v-layout id="top" column justify-center align-center>
    <v-flex xs12 class="main-banner">
      <Logo />
      <div id="content-title" class="title text-center">Percorsi educativi</div>
      <div class="text-center">
        <v-sheet id="main-content" color="white"
          >Il nostro è il metodo di educazione detto gentile, adatto a qualunque
          cane, indipendentemente da razza, età, sesso e caratteristiche
          individuali, e personalizzato con uno studio attento dell’animale
          affinché possa offrire la massima efficacia. Durante un percorso di
          educazione, cane e proprietario imparano, insieme, gli esercizi di
          base utili nella vita quotidiana, come la condotta al guinzaglio e il
          richiamo, ma soprattutto a relazionarsi nel migliore dei modi, a
          risolvere piccoli e grandi problemi ed avere così una vita insieme più
          felice e semplice per entrambi.
        </v-sheet>
        <div class="media1">
          <v-img :src="asilo1" />
        </div>
        <v-card
          class="mx-auto"
          width="85vw"
          color="#26c6da"
          dark
          max-width="400"
        >
          <v-card-title>
            <v-icon large left>
              mdi-paw
            </v-icon>
            <span class="title font-weight-light">Puppy School</span>
          </v-card-title>

          <v-card-text class="headline font-weight-bold">
            Gli obiettivi di questo percorso sono diversi e contribuiscono tutti
            al benessere di cucciolo e proprietario e alla crescita serena del
            nostro piccolo amico.
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
                <v-btn outlined color="purple" text to="./puppy-school">
                  Scopri
                </v-btn>
              </v-row>
            </v-list-item>
          </v-card-actions>
        </v-card>
        <v-sheet id="main-content" color="white"
          >Se invece sei alla ricerca del tuo amico peloso, ti offriamo la
          migliore consulenza, competente e attenta, che ti guidi in un percorso
          di adozione maturo e responsabile.
        </v-sheet>
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
  name: 'Percorsi',
  components: {
    Logo
    // Breadcrumbs
  },

  data() {
    return {
      imgSrc: this.$route.name,
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

<style lang="scss" scoped>
@import '~/assets/content.scss';
</style>
