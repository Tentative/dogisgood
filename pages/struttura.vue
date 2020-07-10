<template>
  <v-layout id="top" column justify-center align-center>
    <v-flex xs12 class="main-banner">
      <Logo />
      <div id="content-title" class="title text-center">La struttura</div>
      <div class="text-center">
        <v-sheet id="main-content" color="white"
          >La struttura che ospita l’Asilo Dog is Good è stata realizzata per
          rispondere al meglio a tutte le esigenze dei nostri amici pelosi e
          offrire comfort, igiene e sicurezza adeguati al loro benessere. 400 mq
          e un ampio cortile privato a disposizione.
        </v-sheet>
        <iframe
          frameborder="0"
          style="border:0"
          src="https://www.google.com/maps/embed/v1/place?key=AIzaSyCM9Ft7KvSSTRPOzXmHaRo583-JqEifRQY&q=Dog+is+Good,+Via+S.+Vitale,+129,+20831+Seregno+MB/@45.6562345,9.2024461,15z/data=!4m5!1m2!2m1!1smaps+asilo+dog+is+good!3m1!1s0x4786bd09259b16ff:0x37f2511351fa4b67"
          allowfullscreen
        >
        </iframe>
        <div class="media1">
          <v-img :src="struttura1" />
        </div>
        <div class="media1">
          <v-img :src="struttura2" />
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
      struttura2: require('@/static/struttura2.jpg')
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
