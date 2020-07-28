<template>
  <div>
    <v-row id="container_row" align="end" :style="style">
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
          <v-row align="end" align-content="space-between">
            <v-col :cols="7"
              >Asilo per cani dog is good
              <div class="social_sub">
                Via S. Vitale, 129, 20831 Seregno MB, Italia
              </div>

              <div class="social_sub_icon">
                <v-icon color="white">mdi-phone</v-icon>
                <v-icon>mdi-email</v-icon>
                <v-icon>mdi-whatsapp</v-icon>
              </div>
            </v-col>
            <v-col :cols="5">
              <Maps />
            </v-col>
          </v-row>
        </v-row>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import { Maps } from '@/components/'
import tiktok from '@/components/tiktok.vue'
export default {
  name: 'End',
  components: {
    tiktok,
    Maps
  },
  props: ['is_toelettatura'],
  data() {
    return {
      src: require('@/static/logo-circle.png'),
      style: this.is_toelettatura ? 'background-color:#3f51b5 ' : ''
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/FooterLarge.scss';
</style>
