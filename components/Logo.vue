<template>
  <div class="main-banner">
    <v-img :src="banner" />
  </div>
</template>

<script>
export default {
  props: {
    imgSrc: {
      type: String,
      required: true
    }
  },
  data() {
    return {
      banner: require(`@/static/${this.imgSrc}-banner-mobile.jpg`)
    }
  }
}
</script>
<style lang="scss" scoped>
@import '@/assets/logo.scss';
</style>
