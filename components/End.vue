<template>
  <div>
    <v-img id="footer_logo" :src="src" />
    <v-row id="container_row" align="end">
      <v-col class="container_col_sx" :cols="6">
        <v-row class="empty_row"> </v-row>
        <v-row class="short_row">
          <v-col :cols="7">
            <v-row class="social">
              <div>Seguici sui nostri social!</div>
            </v-row>
          </v-col>
          <v-col :cols="5">
            <v-row justify="center">
              <a
                id="footer_link_1"
                href="https://www.tiktok.com/@asilodogisgood"
                target="_blank"
                ><div class="tiktok_end">
                  <tiktok /></div
              ></a>
              <a
                id="footer_link_2"
                href="https://www.facebook.com/asilodogisgood/"
                target="_blank"
                ><div><v-icon size="38px">mdi-facebook</v-icon></div></a
              >
              <a
                id="footer_link_3"
                href="https://www.instagram.com/asilodogisgood/"
                target="_blank"
                ><div><v-icon size="38px">mdi-instagram</v-icon></div></a
              >
              <a
                id="footer_link_4"
                href="https://www.instagram.com/asilodogisgood/"
                target="_blank"
                ><div>
                  <v-icon size="38px" color="red">mdi-youtube</v-icon>
                </div></a
              >
            </v-row>
          </v-col>
        </v-row>
      </v-col>
      <v-col class="container_col_dx" :cols="6">
        <v-row class="high_row social">
          <v-row align="center" justify="center" align-content="space-between">
            <v-col :cols="7"
              >Asilo per cani dog is good
              <div class="social_sub">
                Via S. Vitale, 129, 20831 Seregno MB, Italia
              </div>

              <div class="social_sub_icon">
                <v-btn text icon color="white" class="mx-5"
                  ><v-icon>mdi-phone</v-icon></v-btn
                >
                <v-btn
                  href="mailto:info.dogisgood@gmail.com"
                  class="mx-5"
                  text
                  icon
                  ><v-icon>mdi-email</v-icon></v-btn
                >
                <v-btn href="https://wa.me/393397268386" class="mx-5" text icon
                  ><v-icon>mdi-whatsapp</v-icon></v-btn
                >
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
