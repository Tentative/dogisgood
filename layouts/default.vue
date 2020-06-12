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
            <span>
              <v-list-item-title v-text="item.title" />
            </span>
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
      <v-img icon @click.stop="rightDrawer = !rightDrawer">
        <v-icon>mdi-menu</v-icon>
      </v-img>
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
    <v-footer :fixed="fixed" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
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
