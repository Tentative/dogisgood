<template>
  <div style="position:relative">
    <v-layout id="top" column justify-center align-center>
      <Logo class="hidden-md-and-up" :src="src_logo" style="width:100%" />

      <section id="content_large" :style="style" class="hidden-sm-and-down">
        <v-container
          style="background-color:rgba(0,0,0,0.6);height:100vh"
          align-center
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
            align="center"
          >
            <v-col :cols="6">
              <v-row class="mx-auto" justify="center" align="center">
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
                  <v-btn icon href="https://www.tiktok.com/@asilodogisgood"
                    ><tiktok
                  /></v-btn>
                </div>
                <v-btn
                  icon
                  href="https://m.facebook.com/asilodogisgood/"
                  :ripple="false"
                  ><v-icon size="38px">mdi-facebook</v-icon></v-btn
                >
                <v-btn
                  icon
                  href="https://www.instagram.com/asilodogisgood/"
                  :ripple="false"
                  ><v-icon size="38px">mdi-instagram</v-icon></v-btn
                >
                <v-btn icon href="https://wa.me/393397268386" :ripple="false"
                  ><v-icon size="38px">mdi-whatsapp</v-icon></v-btn
                >
              </v-row>
            </v-col>
            <v-col :cols="6" class="pa-5">
              <v-sheet
                color="white"
                class="text-center pa-5"
                style="margin-bottom:20px"
              >
                <Maps />
                Via San Vitale, 129, Seregno (MB)</v-sheet
              >
            </v-col>

            <v-row id="main_row" justify="center" class="mt-5">
              <v-row justify="center" style="width:100%" class="mt-5 pt-5">
                <div id="partners" class="text-center mx-auto display-3">
                  I nostri partner:
                </div>
              </v-row>
              <v-col
                v-for="partner in partners"
                :key="partner"
                cols="4"
                class="mx-auto"
                style="text-align:center"
              >
                <v-avatar size="48">
                  <v-img :src="partner.icon" />
                </v-avatar>
              </v-col>
              <FooterLarge class="hidden-sm-and-down" style="width:100%" />
            </v-row>
          </v-row>
        </v-container>
      </section>
      <section class="hidden-md-and-up">
        <div
          id="main-content"
          class="text-center title ma-5 text-uppercase blue white--text"
        >
          CONTATTACI
        </div>
        <v-sheet style="max-width:85vw" class="mx-auto">
          <v-row class="mx-auto" justify="center" align="center">
            <div class="text-center">
              <v-sheet
                color="white"
                class="text-center transparent"
                style="margin-bottom:20px"
              >
                <v-row class="mx-auto" justify="center">
                  <v-btn
                    class="pa-5 text-truncate"
                    tile
                    block
                    outlined
                    color="success"
                    href="mailto:info.dogisgood@gmail.com"
                  >
                    <v-icon size="32px" left>mdi-email</v-icon>
                    <span class="text-truncate">info</span>
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
              <Maps class="hidden-md-and-up" />
            </div>
          </v-row>
        </v-sheet>
      </section>

      <!-- 
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
    </v-fab-transition> -->
      <!-- <Breadcrumbs :levels="1" /> -->
    </v-layout>
  </div>
</template>

<script>
import { Maps, tiktok, Logo, FooterLarge } from '@/components'
// import Breadcrumbs from '@/components/Breadcrumbs.vue'
export default {
  name: 'CampoEducazionePrivato',
  components: {
    Logo,
    Maps,
    tiktok,
    FooterLarge
    // Breadcrumbs
  },

  data() {
    return {
      imgSrc: 'osteopatia animale',
      mobile: 'tel:+393397268386',
      tt: require('@/static/tik-tok.png'),
      phone: 'tel:+3903621821674',
      partners: [
        {
          icon: require('@/static/partners/gammavet.png')
        },
        {
          icon: require('@/static/partners/lussianinda.png')
        },
        {
          icon: require('@/static/partners/mariani.png')
        }
      ],
      mail: 'mailto:info.dogisgood@gmail.com',
      src: require('@/static/logo-circle.png'),
      src_logo: require('@/static/struttura-banner-mobile.jpg'),

      style:
        'background:url(' +
        require('@/static/struttura-banner-mobile.jpg') +
        ');background-size:cover;background-position:center;height:100vh',
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
iframe {
  width: 100%;
  margin-top: 20px;
  height: 350px !important;
  max-height: 600px;
}
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
  & .v-btn {
    padding: 40px;
  }
  & .theme--light.v-btn.v-btn--icon .mdi-facebook {
    color: $facebook;
  }
  & .theme--light.v-btn.v-btn--icon .mdi-instagram {
    color: $instagram;
  }
  & .theme--light.v-btn.v-btn--icon .mdi-whatsapp {
    color: $whatsapp;
  }
}

#end {
  background-color: #2196f3;
}

@import '~/assets/content.scss';
@import '~/assets/end.scss';
@import '~/assets/variables.scss';
</style>
