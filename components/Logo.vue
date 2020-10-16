<template>
  <div class="main-banner">
    <v-img
      id="logo"
      :src="src"
      gradient="to top right, rgba(0,0,0,.5), rgba(0,0,0,.3)"
      class="hidden-sm-and-down"
    >
    </v-img>
    <v-img id="logo" :src="src" class="hidden-md-and-up"></v-img>
  </div>
</template>

<script>
export default {
  props: ['src'],
  data() {
    return {
      banner: require(`@/static/${this.$route.name}-banner-mobile.jpg`)
    }
  }
  // computed: {
  //   width() {
  //     return window.innerWidth > 1200
  //       ? 'to top right, rgba(0,0,0,.5), rgba(0,0,0,.3)'
  //       : ''
  //   },
  //   isMobile() {
  //     return window.innerWidth < 768
  //   }
  // }
}
</script>
<style lang="scss" scoped>
@import '@/assets/logo.scss';
</style>
