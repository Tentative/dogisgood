<template>
  <div>
    <v-row id="container_row" align="end" :style="style">
      <v-col class="container_col_sx" :cols="6">
        <v-row class="empty_row"> </v-row>
        <v-row class="short_row">
          <v-col :cols="5" align-self="center">
            <v-row class="social title">
              <div>Seguici sui nostri social!</div>
            </v-row>
          </v-col>
          <v-col :cols="7" align-self="center">
            <v-row justify="center" align="center" align-content="center">
              <a href="https://www.tiktok.com/@asilodogisgood" target="_blank"
                ><div class="tiktok_end">
                  <tiktok /></div
              ></a>
              <a href="https://www.facebook.com/asilodogisgood/" target="_blank"
                ><div><v-icon size="38px">mdi-facebook</v-icon></div></a
              >
              <a
                href="https://www.instagram.com/asilodogisgood/"
                target="_blank"
                ><div><v-icon size="38px">mdi-instagram</v-icon></div></a
              >
              <a
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
          <v-row align="center" align-content="space-between">
            <v-col :cols="7"
              >Asilo per cani dog is good
              <div class="social_sub">
                Via S. Vitale, 129, 20831 Seregno MB, Italia
              </div>

              <div class="social_sub_icon">
                <v-btn text icon color="white" class="mx-5"
                  ><v-icon>mdi-phone</v-icon></v-btn
                >
                <v-btn href="mailto:info@dogisgood.it" class="mx-5" text icon
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
.v-application a {
  color: transparent !important;
  &:visited {
    color: transparent !important;
  }
}
@import '@/assets/FooterLarge.scss';
</style>
