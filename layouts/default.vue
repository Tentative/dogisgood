<template>
  <v-app light>
    <v-navigation-drawer
      v-model="drawer"
      class="accent"
      :mini-variant="miniVariant"
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
      <v-btn icon @click.stop="clipped = !clipped">
        <v-icon class="white--text">mdi-paw</v-icon>
      </v-btn>
      <v-btn icon @click.stop="fixed = !fixed">
        <v-icon class="white--text">mdi-bone</v-icon>
      </v-btn>
      <v-spacer />
      <v-btn icon @click.stop="rightDrawer = !rightDrawer">
        <v-img src="./root/dogisgood/static/logo-circle-main-nav.png"></v-img>
      </v-btn>
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
    <v-footer light padless>
      <v-card class="flex" flat tile>
        <v-card-title id="footer" class="white--text text-center">
          <div class="subheading ">Seguici sui social:</div>

          <v-spacer></v-spacer>

          <v-btn v-for="icon in icons" :key="icon" class="mx-4" dark icon>
            <v-icon size="24px">{{ icon }}</v-icon>
          </v-btn>
        </v-card-title>

        <v-card-text class="py-2 black--text text-center">
          {{ new Date().getFullYear() }} — <strong>Dog is good</strong>
        </v-card-text>
      </v-card>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      icons: ['mdi-facebook', 'mdi-instagram'],
      items: [
        {
          icon: 'mdi-home',
          title: 'Homepage',
          to: '/'
        },
        {
          icon: 'mdi-checkbox-marked-circle-outline',
          title: 'Servizi',
          to: '/inspire'
        },
        {
          icon: 'mdi-google-maps',
          title: 'Dove trovarci',
          to: '/contact-us'
        },
        {
          icon: 'mdi-view-carousel',
          title: 'Gallery',
          to: '/gallery'
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
