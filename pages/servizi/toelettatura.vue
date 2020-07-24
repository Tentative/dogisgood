<template>
  <v-layout id="top" column justify-center align-center>
    <v-flex xs12 class="main-banner">
      <Logo />
      <div id="content-title" class="title text-center">Toelettatura</div>
      <div id="content-subtitle" class="subtitle-2 text-center">
        Toelettatura Dog is Good by Spelacchio!
      </div>

      <div class="text-center">
        <v-sheet
          id="main-content"
          class="text-center"
          color="white"
          style="margin-top: 20px"
        >
          <v-img :src="Toelettatura" height="300px" dark>
            <v-row class="fill-height">
              <v-spacer></v-spacer>

              <v-card-subtitle
                class="white--text  pt-12 mt-12"
                style="padding-top:40%!important"
              >
                <div class="headline  pt-12 mt-12">Servizi offerti:</div>
              </v-card-subtitle>
            </v-row>
          </v-img>

          <v-list two-line>
            <v-list-item>
              <v-list-item-icon>
                <v-icon color="indigo">mdi-shower</v-icon>
              </v-list-item-icon>

              <v-list-item-content>
                <v-list-item-title>Bagni di igiene</v-list-item-title>
              </v-list-item-content>
            </v-list-item>

            <v-divider inset></v-divider>

            <v-list-item>
              <v-list-item-icon>
                <v-icon color="indigo">mdi-content-cut</v-icon>
              </v-list-item-icon>

              <v-list-item-content>
                <v-list-item-title>Taglio a forbice</v-list-item-title>
              </v-list-item-content>
            </v-list-item>

            <v-divider inset></v-divider>

            <v-list-item>
              <v-list-item-icon>
                <v-icon color="indigo">mdi-scissors-cutting</v-icon>
              </v-list-item-icon>

              <v-list-item-content>
                <v-list-item-title>Tosatura</v-list-item-title>
              </v-list-item-content>
            </v-list-item>

            <v-divider inset></v-divider>

            <v-list-item>
              <v-list-item-icon>
                <v-icon color="indigo">mdi-hair-dryer</v-icon>
              </v-list-item-icon>

              <v-list-item-content>
                <v-list-item-title>Snodatura</v-list-item-title>
              </v-list-item-content>
            </v-list-item>

            <v-divider inset></v-divider>

            <v-list-item>
              <v-list-item-icon>
                <v-icon color="indigo">mdi-filmstrip-off</v-icon>
              </v-list-item-icon>

              <v-list-item-content>
                <v-list-item-title>Stripping</v-list-item-title>
              </v-list-item-content>
            </v-list-item>

            <v-divider inset></v-divider>

            <v-list-item>
              <v-list-item-icon>
                <v-icon color="indigo">mdi-dog</v-icon>
              </v-list-item-icon>

              <v-list-item-content>
                <v-list-item-title class="text-no-wrap"
                  >Pulizia orecchie
                </v-list-item-title>
                <v-list-item-title>e taglio unghie</v-list-item-title>
              </v-list-item-content>
            </v-list-item>

            <v-divider inset></v-divider>

            <v-list-item>
              <v-list-item-icon>
                <v-icon color="indigo">mdi-palette</v-icon>
              </v-list-item-icon>

              <v-list-item-content>
                <v-list-item-title class="text-no-wrap"
                  >Cromoterapia
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>

            <v-divider inset></v-divider>

            <v-list-item>
              <v-list-item-icon>
                <v-icon color="indigo">mdi-cat</v-icon>
              </v-list-item-icon>

              <v-list-item-content>
                <v-list-item-title class="text-no-wrap"
                  >Toelettatura sanitaria
                </v-list-item-title>
                <v-list-item-title>gatti</v-list-item-title>
              </v-list-item-content>
            </v-list-item>

            <v-divider inset></v-divider>

            <v-list-item style="width:100%;padding:0;">
              <!-- <v-list-item-icon>
                <v-icon color="indigo">mdi-shower-head</v-icon>
              </v-list-item-icon> -->

              <v-list-item-content>
                <v-expansion-panels>
                  <v-expansion-panel>
                    <v-expansion-panel-header color="blue" class="white--text"
                      >Bagno </v-expansion-panel-header
                    ><v-expansion-panel-content
                      class="body-1"
                      style="width:100%"
                    >
                      Con acqua ozonizzata. Dona lucentezza, apre i nodi,
                      elimina zecche e pulci, efficace contro dermatosi e
                      micosi, disinfetta e aiuta la cicatrizzazione di ferite.
                    </v-expansion-panel-content></v-expansion-panel
                  >
                </v-expansion-panels>
              </v-list-item-content>
            </v-list-item>

            <v-divider inset></v-divider>

            <v-list>
              <v-list-item-content>
                <v-expansion-panels>
                  <v-expansion-panel>
                    <v-expansion-panel-header color="blue" class="white--text"
                      >SPA</v-expansion-panel-header
                    ><v-expansion-panel-content
                      class="body-1"
                      style="width:100%"
                    >
                      Con idromassaggio che riduce la tensione nervosa ed ha un
                      effetto rilassante, massaggio a fondo la cute e tonifica
                      la muscolatura.
                    </v-expansion-panel-content></v-expansion-panel
                  >
                </v-expansion-panels>
              </v-list-item-content>
              <v-divider inset></v-divider>
            </v-list>
          </v-list>
          <v-row justify="center">
            <div id="content-title" class="title">
              Venite a trovarci!
            </div>
            <div class="body-2">
              Per info e appuntamenti:
            </div>
          </v-row>
          <v-row justify="center" style="margin-top:20px">
            <v-card class="mx-auto" max-width="300" tile>
              <v-img height="100%" :src="Toelettatura">
                <v-row align="end" class="fill-height">
                  <v-col align-self="start" class="pa-0" cols="12">
                    <v-avatar class="profile" color="grey" size="164" tile>
                      <v-img :src="spelacchio"></v-img>
                    </v-avatar>
                  </v-col>
                  <v-col class="py-0">
                    <v-list-item color="rgba(0, 0, 0, .4)" dark>
                      <v-list-item-content>
                        <v-list-item-title class="title"
                          >SPELACCHIO</v-list-item-title
                        >
                        <v-list-item-subtitle class="title"
                          ><a
                            class="white--text"
                            href="mailto:spelacchiodog@gmail.com"
                            >spelacchiodog@gmail.com</a
                          ></v-list-item-subtitle
                        >
                      </v-list-item-content>
                    </v-list-item>
                  </v-col>
                </v-row>
              </v-img>
            </v-card>
          </v-row>
        </v-sheet>
      </div>
    </v-flex>
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
import Logo from '@/components/Logo.vue'
// import Breadcrumbs from '@/components/Breadcrumbs.vue'
export default {
  name: 'Struttura',
  components: {
    Logo
    // Breadcrumbs
  },

  data() {
    return {
      show: false,
      spelacchio: require('@/static/spelacchio-logo grande.jpeg'),
      showspa: false,
      imgSrc: 'struttura',
      fab: false,
      offsetTop: 0,
      bagno: require('@/static/bagno-ozonizzante.jpg'),
      spa: require('@/static/spa.jpg'),
      Toelettatura: require('@/static/servizi-toelettatura-banner-mobile.jpg')
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

<style lang="scss">
@import '~/assets/content.scss';
</style>
