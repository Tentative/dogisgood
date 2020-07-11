<template>
  <v-app light>
    <v-navigation-drawer
      v-model="drawer"
      color="white"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar :clipped-left="clipped" fixed app class="primary">
      <v-app-bar-nav-icon class="white--text" @click.stop="drawer = !drawer" />

      <v-btn icon @click.stop="miniVariant = !miniVariant">
        <v-icon class="white--text">mdi-home</v-icon>
      </v-btn>

      <v-spacer />
      <v-list-item-avatar color="grey darken-3">
        <v-img class="elevation-6" :src="logoSrc"></v-img>
      </v-list-item-avatar>
    </v-app-bar>
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
    <v-navigation-drawer v-model="rightDrawer" :right="right" temporary fixed>
      <v-list>
        <v-list-item @click.native="right = !right">
          <v-list-item-action>
            <v-icon light>
              mdi-repeat
            </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer (click me)</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
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
          icon: 'mdi-bone',
          title: 'Percorsi',
          to: '/percorsi'
        },
        {
          icon: 'mdi-donkey',
          title: 'Toelettatura',
          to: 'servizi/toelettatura'
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
