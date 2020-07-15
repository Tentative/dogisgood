<template>
  <v-app light>
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>

    <Footer />
  </v-app>
</template>

<script>
import Footer from '@/components/Footer.vue'
export default {
  name: 'Home',
  components: {
    Footer
  },
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      logoSrc: require('@/static/logo.jpg'),
      icons: ['mdi-whatsapp', 'mdi-facebook', 'mdi-instagram'],
      items: [
        {
          icon: 'mdi-home',
          title: 'Homepage',
          to: '/'
        },
        {
          icon: 'mdi-paw',
          title: 'Asilo',
          to: '/asilo'
        },
        {
          icon: 'mdi-donkey',
          title: 'Toelettatura',
          to: 'servizi/toelettatura'
        },
        {
          icon: 'mdi-bone',
          title: 'Percorsi educativi',
          to: '/percorsi'
        },
        {
          icon: 'mdi-email',
          title: 'Contatti',
          to: '/contattaci'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'DogIsGood - Asilo per cani'
    }
  }
}
</script>

<style lang="scss">
@import '@/assets/homepage.scss';
</style>
