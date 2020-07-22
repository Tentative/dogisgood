<template>
  <v-layout id="top" column justify-center align-center>
    <v-flex xs12 class="main-banner">
      <Logo :src="asilo_src" />
      <div id="content-title" class="title text-center">L'asilo</div>
      <v-col xs="12" sm="12" md="7">
        <div class="text-center">
          <v-sheet id="main-content" color="white" style="margin-bottom:20px"
            >Il nostro cane è un compagno di vita e condivide con noi avventure
            e tempo libero, ma gli impegni quotidiani, spesso, ci tengono fuori
            casa per parecchie ore costringendo il nostro amico a rimanere solo
            e recluso. L’idea del nostro asilo nasce proprio da una riflessione
            intorno alle esigenze di entrambi. L’asilo è lo spazio dove il
            nostro cane può giocare, correre, riposarsi, uscire nel nostro
            cortile privato e fare tante attività nel nostro grande campo di
            educazione.
          </v-sheet>

          <v-sheet id="content" color="white">
            Può vivere quindi nel migliore dei modi quella esperienza di
            socializzazione fondamentale per il suo benessere psicofisico,
            sempre sotto la sorveglianza attenta frutto dei nostri studi di
            educazione cinofila. Perché un cane educato e stanco è un cane
            felice, con un proprietario sereno e contento. L’asilo è quindi il
            luogo che può, con competenza e serietà, sostituirsi al suo compagno
            umano nei momenti di assenza, quando sono necessarie attenzioni
            particolari sia per i cuccioli, sia per i soggetti molto anziani, o
            anche semplicemente quando le condizioni atmosferiche non ci
            consentono lunghe passeggiate. Affinché tutti i cani possano
            interagire nella maniera migliore, ogni nostro ospite usufruirà di
            un’ora di prova gratuita per comprendere se l’asilo è il posto
            migliore per lui e se necessita eventualmente di un percorso di
            inserimento.
          </v-sheet>
        </div>
      </v-col>

      <div class="media1">
        <v-img :src="asilo1" />
      </div>
      <div id="content-title" class="text-center title">
        Il nostro asilo è aperto
      </div>
      <div class="text-center subtitle-2" style="margin-bottom:20px">
        dal lunedì al venerdì, dalle 7.30 alle 19
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
  name: 'Asilo',
  components: {
    Logo
    // Breadcrumbs
  },

  data() {
    return {
      imgSrc: this.$route.name,
      asilo_src: require('@/static/asilo-banner-mobile.jpg'),
      fab: false,
      offsetTop: 0,
      asilo1: require('@/static/asilo-1.jpg')
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
