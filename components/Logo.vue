<template>
  <div class="main-banner">
    <v-img id="logo" :src="src" :gradient="width">
      <v-btn
        v-show="!isMobile"
        id="to-bottom"
        absolute
        dark
        fab
        bottom
        center
        small
        color="#5ea5ef"
        @click="$vuetify.goTo('#top', 2500)"
      >
        <v-icon>mdi-chevron-down</v-icon>
      </v-btn>
    </v-img>
  </div>
</template>

<script>
export default {
  props: ['src'],
  data() {
    return {
      banner: require(`@/static/${this.$route.name}-banner-mobile.jpg`)
    }
  },
  computed: {
    width() {
      return window.innerWidth > 1200
        ? 'to top right, rgba(0,0,0,.5), rgba(0,0,0,.3)'
        : ''
    },
    isMobile() {
      return window.innerWidth < 768
    }
  }
}
</script>
<style lang="scss" scoped>
@import '@/assets/logo.scss';
</style>
