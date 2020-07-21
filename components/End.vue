<template>
  <div>
    <v-img id="footer_logo" :src="src" />
    <v-row id="container_row">
      <v-col class="container_col_sx" :cols="6">
        <v-row class="empty_row"> </v-row>
        <v-row class="short_row">
          <v-col :cols="7">
            <v-row class="social">
              <div>Seguici sui nostri social!</div>
            </v-row>
          </v-col>
          <v-col :cols="5">
            <v-row>
              <div class="tiktok_end"><tiktok /></div>
              <v-icon size="38px">mdi-facebook</v-icon>
              <v-icon size="38px">mdi-instagram</v-icon>
            </v-row>
          </v-col>
        </v-row>
      </v-col>
      <v-col class="container_col_dx" :cols="6">
        <v-row class="high_row social">
          <v-col :cols="7">Asilo per cani dog is good</v-col></v-row
        >
        <v-row>asdasd</v-row>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import tiktok from '@/components/tiktok.vue'
export default {
  name: 'End',
  components: {
    tiktok
  },
  data() {
    return {
      src: require('@/static/logo-circle.png')
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/end.scss';
</style>
