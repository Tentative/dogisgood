<template>
  <v-layout id="top" column justify-center align-center>
    <Logo class="hidden-md-and-up" />
    <section id="content_large" :style="style">
      <v-container
        class="hidden-sm-and-down"
        style="background-color:rgba(0,0,0,0.4)"
      >
        <v-row id="main_row" justify="center">
          <v-col :cols="12">
            <div
              id="content-title"
              class="  text-center display-4"
              style="color:white"
            >
              Contattaci
            </div>
          </v-col>
        </v-row>
        <v-row
          id="main_row"
          class="mx-auto"
          justify="center"
          style="width:100%"
        >
          <v-col :cols="6">
            <v-row class="mx-auto" justify="center">
              <div class="text-center">
                <v-sheet
                  color="white"
                  class="text-center transparent"
                  style="margin-bottom:20px"
                >
                  <v-row class="mx-auto" justify="center">
                    <v-btn
                      class="pa-5"
                      tile
                      block
                      outlined
                      color="success"
                      href="mailto:info.dogisgood@gmail.com"
                    >
                      <v-icon size="32px" left>mdi-email</v-icon>
                      info.dogisgood@gmail.com
                    </v-btn>
                  </v-row></v-sheet
                >

                <v-sheet
                  color="white"
                  class="text-center mt-2 transparent"
                  style="margin-bottom:20px"
                >
                  <v-row class="mx-auto" justify="center">
                    <v-btn
                      class="pa-5"
                      tile
                      block
                      outlined
                      color="success"
                      href="tel:+393397268386"
                    >
                      <v-icon size="32px" left>mdi-cellphone</v-icon>
                      339-7268386
                    </v-btn>
                  </v-row></v-sheet
                >
                <v-sheet
                  color="white"
                  class="text-center transparent"
                  style="margin-bottom:20px"
                >
                  <v-row class="mx-auto" justify="center">
                    <v-btn
                      class="pa-5"
                      tile
                      block
                      outlined
                      color="success"
                      href="tel:+3903621821674"
                    >
                      <v-icon size="32px" left>mdi-deskphone</v-icon>
                      0362-1821674
                    </v-btn>
                  </v-row></v-sheet
                >
              </div>
            </v-row>

            <v-row
              id="social"
              class="mx-auto social social_sub_icon"
              justify="center"
            >
              <div class="tt_end " style="padding-right:20px">
                <a href="www.google.com"><tiktok /></a>
              </div>
              <v-btn icon href="www.google.it" :ripple="false"
                ><v-icon size="38px">mdi-facebook</v-icon></v-btn
              >
              <v-icon size="38px">mdi-instagram</v-icon>
              <v-icon>mdi-whatsapp</v-icon>
            </v-row>
          </v-col>
          <v-col :cols="6">
            <v-sheet
              color="white"
              class="text-center"
              style="margin-bottom:20px"
            >
              <Maps />
              Via San Vitale, 129, Seregno (MB)</v-sheet
            >
          </v-col>
        </v-row>
        <v-row id="main_row" justify="center"> </v-row>
      </v-container>
    </section>

    <v-fab-transition>
      <v-btn
        v-show="fab"
        id="to-top"
        v-scroll="onScroll"
        fixed
        dark
        fab
        bottom
        right
        small
        color="pink"
        @click="$vuetify.goTo('#top', 2500)"
      >
        <v-icon>mdi-chevron-up</v-icon>
      </v-btn>
    </v-fab-transition>
    <!-- <Breadcrumbs :levels="1" /> -->
  </v-layout>
</template>

<script>
import { Logo, Maps, tiktok } from '@/components'
// import Breadcrumbs from '@/components/Breadcrumbs.vue'
export default {
  name: 'CampoEducazionePrivato',
  components: {
    Logo,
    Maps,
    tiktok
    // Breadcrumbs
  },

  data() {
    return {
      imgSrc: 'osteopatia animale',
      mobile: 'tel:+393397268386',
      tt: require('@/static/tik-tok.png'),
      phone: 'tel:+3903621821674',
      mail: 'mailto:info.dogisgood@gmail.com',

      style:
        'background:url(' +
        require('@/static/struttura-banner-mobile.jpg') +
        ');background-size:cover;background-position:center;',
      fab: false,
      offsetTop: 0,
      struttura1: require('@/static/struttura3.jpg'),
      struttura2: require('@/static/struttura2.jpg')
    }
  },
  methods: {
    onScroll(e) {
      if (typeof window === 'undefined') return
      const top = window.pageYOffset || e.target.scrollTop || 0
      this.fab = top > 200
    }
  },
  layout: 'homepage'
}
</script>

<style lang="scss" scoped>
.tt_end {
  // padding: 20px;
  display: flex;
  align-items: center;
  height: 34px;
  & svg {
    fill: white !important;
    height: 34px !important;
    width: 34px;
  }
}

.mdi-whatsapp {
  font-size: 38px;
  color: #00e676;
}

#social {
  &
}
@import '~/assets/content.scss';
@import '~/assets/end.scss';
</style>
