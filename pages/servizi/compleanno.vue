<template>
  <v-layout id="top" column justify-center align-center>
    <v-flex xs12 class="main-banner">
      <Logo />
      <div id="content-title" class="title text-center">
        Feste di compleanno
      </div>

      <div class="text-center">
        <v-sheet id="main-content" color="white" style="margin-bottom:20px"
          >Il tuo migliore amico compie gli anni? Festeggia insieme a noi!
          L'Asilo per Cani Dog is Good ti offre una vera festa a quattro zampe:
          Torta esclusivamente artigianale con ingredienti adatti al tuo cane e
          ai suoi ospiti Animazione dedicata seguita dai nostri esperti
          educatori cinofili 1 foto 20x30 cm con zampa ricordo del tuo amico
          peloso Foto in digitale del servizio fotografico Buonissimi e golosi
          gadget personalizzati da regalare agli invitati
        </v-sheet>
        <div id="content-title" class="text-center title">
          <v-btn block color="#21f37e" to="/contact-us">contattaci</v-btn>

          per avere più informazioni!
        </div>

        <div class="media1">
          <v-img :src="compleanno1" />
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
      compleanno1: require('@/static/compleanno.jpg')
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
