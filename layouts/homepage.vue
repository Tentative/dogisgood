<template>
  <v-app id="main_app" light>
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
    <v-app-bar :clipped-left="clipped" app class="primary">
      <v-app-bar-nav-icon class="white--text" @click.stop="drawer = !drawer" />

      <v-btn
        :class="top > 200 && !isMobile ? 'hamburger_hide' : 'hamburger_show'"
        icon
        to="/"
        @click.stop="miniVariant = !miniVariant"
      >
        <v-icon class="white--text">mdi-home</v-icon>
      </v-btn>

      <v-spacer />
      <v-list-item-avatar color="grey darken-3">
        <v-img
          class="elevation-6 logo_drawer"
          :src="logoSrc"
          @click.stop="drawer = !drawer"
        ></v-img>
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
    <Footer class="hidden-md-and-up" />
  </v-app>
</template>

<script>
import { Footer } from '@/components/'
export default {
  name: 'Home',
  components: {
    Footer
    // FooterLarge
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
      title: 'DogIsGood - Asilo per cani',
      fix: !this.isMobile,
      bar_color: top > 200 && !this.isMobile ? 'transparent' : '#5ea5ef',
      top: 0
    }
  },
  computed: {
    isMobile() {
      return !(window.innerWidth > 768)
    }
  },

  beforeMount() {
    window.addEventListener('scroll', this.handleScroll)
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll)
  },

  methods: {
    handleScroll() {
      // Your scroll handling here
      // console.log(window.scrollY)
      this.top = window.scrollY
    }
  }
}
</script>

<style lang="scss">
@import '@/assets/homepage.scss';
</style>
