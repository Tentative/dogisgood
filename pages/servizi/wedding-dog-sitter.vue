<template>
  <v-layout id="top" column justify-center align-center>
    <v-flex xs12 class="main-banner">
      <Logo />
      <div id="content-title" class="title text-center">Wedding Dog Sitter</div>
      <div id="content-subtitle" class="subtitle-2 text-center">
        Perché rinunciare al tuo migliore amico in uno dei giorni più belli? Con
        Dog is Good tutto è possibile!
      </div>
      <div class="text-center">
        <v-sheet id="main-content" color="white" style="margin-bottom:20px"
          >Ci prenderemo cura di lui per tutta la giornata, assicurandoci che ci
          sia nei momenti più importanti. Un membro del nostro team a
          disposizione, un corredino firmato Lussianinda, un reportage della sua
          giornata... cosa chiedere di più? Averlo al tuo fianco sarà uno dei
          ricordi più belli!
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
      imgSrc: 'struttura',
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
