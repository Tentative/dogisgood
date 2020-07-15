<template>
  <div class="main-banner">
    <v-img
      id="logo"
      :src="banner"
      gradient="to top right, rgba(100,115,201,.33), rgba(0,0,0,.7)"
    />
  </div>
</template>

<script>
export default {
  data() {
    return {
      banner: require(`@/static/${this.$route.name}-banner-mobile.jpg`)
    }
  }
}
</script>
<style lang="scss" scoped>
@import '@/assets/logo.scss';
</style>
