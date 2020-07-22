<template>
  <div class="main-banner">
    <v-img id="logo" :src="src" :gradient="width"> </v-img>
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
