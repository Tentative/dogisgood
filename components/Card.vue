<template>
  <v-card class="mx-auto" max-width="500" style="margin-bottom:20px">
    <v-img
      class="white--text align-end"
      height="150px"
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
</template>

<script>
export default {
  name: 'Card',
  props: ['service', 'img']
}
</script>

<style lang="scss" scoped>
@import '@/assets/card.scss';
</style>
