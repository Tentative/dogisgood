<template>
  <div class="main-banner">
    <v-img :src="imgSrc" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      imgSrc: require('@/static/homepage-banner-mobile.jpg')
    }
  }
}
</script>
<style lang="scss" scoped>
@import '@/assets/logo.scss';
</style>
