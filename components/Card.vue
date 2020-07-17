<template>
  <v-card class="mx-auto" max-width="500">
    <v-img class="white--text align-end" height="150px" :src="img1">
      <v-card-title>{{ service.name }}</v-card-title>
      <v-card-text class="text--primary ">
        <div style="color:white">
          {{ service.text }}
        </div>
      </v-card-text>
    </v-img>

    <!-- <v-card-subtitle class="pb-0">{{ service.subtitle }}</v-card-subtitle> -->

    <!-- <v-card-actions>
      <v-btn color="orange" text>
        Scopri
      </v-btn>
    </v-card-actions> -->
  </v-card>
</template>

<script>
export default {
  name: 'Card',
  props: {
    service: {
      type: Object,
      required: true
    }
  },
  data() {
    return {
      img1: require('@/static/toelettatura-home.jpg')
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/card.scss';
</style>
