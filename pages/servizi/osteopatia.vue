<template>
  <v-layout id="top" column justify-center align-center>
    <v-flex xs12 class="main-banner">
      <Logo />
      <div id="content-title" class="title text-center">Osteopatia Animale</div>
      <div class="text-center">
        <v-sheet id="main-content" color="white"
          >L’osteopatia animale è una disciplina olistica complementare alla
          medicina veterinaria, che si avvale di manipolazioni e mobilizzazioni
          terapeutiche, con lo scopo di promuovere il benessere psico-fisico
          dell’animale a 360°. Numerose sono le problematiche che possono
          beneficiare di questo approccio (disturbi dell’apparato
          muscolo-scheletrico, problematiche viscerali, riabilitazione
          post-chirurgica etc.), in quanto riduce significativamente il dolore e
          l’infiammazione, ripristina il normale movimento somatico e promuove
          la capacità di autoregolazione interna di ogni organismo, senza l’uso
          di farmaci.
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
  name: 'Struttura',
  components: {
    Logo
    // Breadcrumbs
  },

  data() {
    return {
      imgSrc: 'osteopatia animale',
      fab: false,
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
  layout: 'homepage'
}
</script>

<style lang="scss" scoped>
@import '~/assets/content.scss';
</style>
