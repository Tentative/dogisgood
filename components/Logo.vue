<template>
  <div class="main-banner">
    <v-img :src="banner" />
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
