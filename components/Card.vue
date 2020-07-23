<template>
  <div class="right_cards">
    <v-card class="mx-auto" max-width="500" style="margin:3% auto">
      <v-img
        class="white--text align-end on_scale"
        height="20vh"
        :src="img"
        gradient="to top right, rgba(0,0,0,.3), rgba(0,0,0,.1)"
      >
        <v-card-title>{{ service.name }}</v-card-title>
        <v-card-text class="text--primary ">
          <div style="color:white">
            {{ service.text }}
          </div>
        </v-card-text>
      </v-img>
    </v-card>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: ['service', 'img'],
  computed: {
    isXL() {
      return !window.innerWidth > 1904
    },
    isMD() {
      return !window.innerWidth > 768 && window.innerWidth < 1264
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/card.scss';
</style>
