<template>
  <div>
    <div class="hidden-sm-and-down">
      <v-flex>
        <section id="content_large" :style="style">
          <v-container style="background-color:rgba(0,0,0,0.4)">
            <v-row id="main_row" justify="center">
              <v-col :cols="12">
                <div
                  id="content-title"
                  class="  text-center display-4"
                  style="color:white"
                >
                  Toelettatura
                </div>
              </v-col>
            </v-row>
            <v-row id="main_row" justify="center">
              <v-col :cols="12">
                <div class="sub_heading text-center display-3 pa-10">
                  Bellezza e salute del cane sono ciò in cui crediamo, il nostro
                  motto è:<br />
                  "amore, cura e rispetto!".
                </div>
              </v-col>
            </v-row>
            <v-row id="main_row" justify="center"> </v-row>
          </v-container>
        </section>
        <section id="toelettatura_desktop">
          <v-row align="center" class="pa-3">
            <v-col :cols="12" order="2">
              <v-row justify="center">
                <v-item-group
                  v-model="window"
                  class="shrink mx-auto pa-3"
                  mandatory
                  tag="v-flex"
                >
                  <v-item
                    v-for="n in length"
                    :key="n"
                    v-slot:default="{ active, toggle }"
                    class="pa-3"
                    style="display:inline-block"
                  >
                    <div>
                      <v-btn :input-value="active" icon @click="toggle">
                        <v-icon>mdi-record</v-icon>
                      </v-btn>
                    </div>
                  </v-item>
                </v-item-group>
              </v-row>
            </v-col>

            <v-col>
              <v-window
                v-model="window"
                class="elevation-1"
                vertical
                show-arrows
              >
                <v-window-item>
                  <v-card flat>
                    <v-card-text>
                      <v-row class="mb-4" align="center">
                        <v-avatar
                          color="white"
                          class="mr-4"
                          width="140"
                          height="140"
                          tile
                          ><v-img :src="spelacchio" contain
                        /></v-avatar>
                        <strong class="display-2">Servizi offerti:</strong>
                        <v-spacer></v-spacer>
                        <!-- <v-btn icon>
                          <v-icon>mdi-account</v-icon>
                        </v-btn> -->
                      </v-row>
                      <v-row
                        align="center"
                        justify="center"
                        style="width:100;margin-left:auto;margin-right:auto"
                      >
                        <v-col
                          :cols="6"
                          style="margin-left:auto;margin-right:auto"
                        >
                          <v-row class="pa-3 " align="center">
                            <v-icon size="48" color="indigo">mdi-shower</v-icon>
                            <p class="title pa-3">Bagni di igiene</p>
                          </v-row>
                          <v-row class="pa-3" align="center">
                            <v-icon size="48" color="indigo"
                              >mdi-content-cut</v-icon
                            >
                            <p class="title pa-3">Taglio a forbice</p>
                          </v-row>
                          <v-row class="pa-3" align="center">
                            <div style="text-align:left;float:left">
                              <razor />
                            </div>
                            <p class="title pa-3">Tosatura</p>
                          </v-row>
                          <v-row class="pa-3" align="center">
                            <v-icon size="48" color="indigo">mdi-dog</v-icon>
                            <p class="title pa-3">
                              Pulizia orecchie e taglio unghie
                            </p>
                          </v-row>
                        </v-col>
                        <v-col :cols="6">
                          <v-row class="pa-3" align="center">
                            <div style="text-align:left;float:left">
                              <comb />
                            </div>
                            <p class="title pa-3">Snodatura</p>
                          </v-row>
                          <v-row class="pa-3" align="center">
                            <div style="text-align:left;float:left">
                              <stripping />
                            </div>
                            <p class="title pa-3">Stripping</p>
                          </v-row>
                          <v-row class="pa-3" align="center">
                            <v-icon size="48" color="indigo"
                              >mdi-palette</v-icon
                            >
                            <p class="title pa-3">
                              Cromoterapia
                            </p>
                          </v-row>
                          <v-row class="pa-3" align="center">
                            <v-icon size="48" color="indigo">mdi-cat</v-icon>
                            <p class="title pa-3">
                              Toelettatura sanitaria gatti
                            </p>
                          </v-row>
                        </v-col>
                      </v-row>
                    </v-card-text>
                  </v-card>
                </v-window-item>

                <v-window-item>
                  <v-card flat>
                    <v-card-text>
                      <v-row class="mb-4" align="center">
                        <v-avatar
                          color="white"
                          class="mr-4"
                          width="140"
                          height="140"
                          tile
                          ><v-img :src="spelacchio" contain
                        /></v-avatar>
                        <strong class="display-2">Servizi offerti:</strong>
                        <v-spacer></v-spacer>
                        <!-- <v-btn icon>
                          <v-icon>mdi-account</v-icon>
                        </v-btn> -->
                      </v-row>
                      <v-row
                        align="center"
                        justify="center"
                        style="width:100%;margin-left:auto;margin-right:auto"
                      >
                        <v-col
                          :cols="12"
                          style="margin-left:auto;margin-right:auto"
                        >
                          <v-row
                            class="pa-5 mx-5 "
                            align="center"
                            justify="center"
                          >
                            <v-expansion-panels>
                              <v-expansion-panel>
                                <v-expansion-panel-header
                                  class="white--text headline"
                                  color="blue"
                                  >Ozonoterapia</v-expansion-panel-header
                                >
                                <v-expansion-panel-content class="title pa-3">
                                  Bagno con acqua ozonizzata. Dona lucentezza,
                                  apre i nodi, elimina zecche e pulci, efficace
                                  contro dermatosi e micosi, disinfetta e aiuta
                                  la cicatrizzazione di ferite.
                                </v-expansion-panel-content>
                              </v-expansion-panel>
                            </v-expansion-panels>
                          </v-row>

                          <v-row
                            class="pa-5 mx-5 "
                            align="center"
                            justify="center"
                          >
                            <v-expansion-panels>
                              <v-expansion-panel>
                                <v-expansion-panel-header
                                  class="white--text headline"
                                  color="blue"
                                  >SPA</v-expansion-panel-header
                                >
                                <v-expansion-panel-content class="title pa-3">
                                  Idromassaggio che riduce la tensione nervosa
                                  ed ha un effetto rilassante, massaggia a fondo
                                  la cute e tonifica la muscolatura.
                                </v-expansion-panel-content>
                              </v-expansion-panel>
                            </v-expansion-panels>
                          </v-row>
                        </v-col>
                      </v-row>
                    </v-card-text>
                  </v-card>
                </v-window-item>

                <v-window-item>
                  <v-card flat :style="background">
                    <v-card-text>
                      <v-row class="mb-4" align="center">
                        <v-avatar
                          color="white"
                          class="mr-4"
                          width="140"
                          height="140"
                          tile
                          ><v-img :src="spelacchio" contain
                        /></v-avatar>
                        <strong class="display-2">Contatti:</strong>
                        <v-spacer></v-spacer>
                      </v-row>
                      <v-row
                        align="center"
                        justify="center"
                        style="width:100%;margin-left:auto;margin-right:auto"
                      >
                        <v-col :cols="12">
                          <v-row class="pa-3 " align="center" justify="start">
                            <v-col :cols="6" align-self="center">
                              <v-img
                                max-width="250px"
                                height="auto"
                                :src="spelacchio"
                                class="mx-auto"
                              />
                              <v-row justify="center" class="mx-auto">
                                <v-btn
                                  class="ma-2"
                                  tile
                                  outlined
                                  color="success"
                                  href="mailto:spelacchiodog@gmail.com"
                                >
                                  <v-icon size="32px" left>mdi-email</v-icon>
                                  spelacchiodog@gmail.com
                                </v-btn>
                                <v-btn
                                  class="ma-2"
                                  tile
                                  outlined
                                  color="success"
                                  href="tel:+393491011358"
                                >
                                  <v-icon size="32px" left>mdi-phone</v-icon>
                                  349 1011358
                                </v-btn>
                              </v-row>
                            </v-col>
                            <v-col :cols="6">
                              <v-row> </v-row>
                            </v-col>
                          </v-row>
                        </v-col>
                      </v-row>
                    </v-card-text>
                  </v-card>
                </v-window-item>
              </v-window>
            </v-col>
          </v-row>
        </section>
      </v-flex>
    </div>
    <section id="toelettatura_mobile" class="hidden-md-and-up">
      <v-layout id="top" column justify-center align-center>
        <v-flex xs12 class="main-banner">
          <Logo />
          <div id="content-title" class="display-1 text-center">
            Toelettatura
          </div>
          <div id="content-subtitle" class="headline text-center">
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
                  </v-card-subtitle>
                </v-row>
              </v-img>
              <div class="headline text-left mt-2">Servizi offerti:</div>

              <v-list>
                <v-list-item>
                  <v-list-item-icon>
                    <v-icon color="indigo">mdi-shower</v-icon>
                  </v-list-item-icon>

                  <v-list-item-content class="text-left">
                    <v-list-item-title>Bagni di igiene</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>

                <v-divider inset></v-divider>

                <v-list-item>
                  <v-list-item-icon>
                    <v-icon color="indigo">mdi-content-cut</v-icon>
                  </v-list-item-icon>

                  <v-list-item-content class="text-left">
                    <v-list-item-title>Taglio a forbice</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>

                <v-divider inset></v-divider>

                <v-list-item style="max-height:58px">
                  <v-list-item-icon>
                    <div style="text-align:left;float:left">
                      <razor style="width:24px;height:24px;" />
                    </div>
                  </v-list-item-icon>

                  <v-list-item-content class="text-left">
                    <v-list-item-title>Tosatura</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>

                <v-divider inset></v-divider>

                <v-list-item style="max-height:58px">
                  <v-list-item-icon>
                    <div style="text-align:left;float:left">
                      <comb style="width:24px;height:auto;" />
                    </div>
                  </v-list-item-icon>

                  <v-list-item-content class="text-left">
                    <v-list-item-title>Snodatura</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>

                <v-divider inset></v-divider>

                <v-list-item style="max-height:58px">
                  <v-list-item-icon>
                    <div style="text-align:left;float:left">
                      <stripping style="width:24px;height:auto;" />
                    </div>
                  </v-list-item-icon>

                  <v-list-item-content class="text-left">
                    <v-list-item-title>Stripping</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>

                <v-divider inset></v-divider>

                <v-list-item>
                  <v-list-item-icon>
                    <v-icon color="indigo">mdi-dog</v-icon>
                  </v-list-item-icon>

                  <v-list-item-content class="text-left">
                    <v-list-item-title class="text-no-wrap"
                      >Pulizia orecchie e taglio unghie
                    </v-list-item-title>
                  </v-list-item-content>
                </v-list-item>

                <v-divider inset></v-divider>

                <v-list-item>
                  <v-list-item-icon>
                    <v-icon color="indigo">mdi-palette</v-icon>
                  </v-list-item-icon>

                  <v-list-item-content class="text-left">
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

                  <v-list-item-content class="text-left">
                    <v-list-item-title class="text-no-wrap"
                      >Toelettatura sanitaria gatti
                    </v-list-item-title>
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
                        <v-expansion-panel-header
                          color="blue"
                          class="white--text"
                          >Ozonoterapia </v-expansion-panel-header
                        ><v-expansion-panel-content
                          class="body-1 pa-2 text-left"
                          style="width:100%"
                        >
                          Bagno con acqua ozonizzata. <br />Dona lucentezza,
                          apre i nodi, elimina zecche e pulci, efficace contro
                          dermatosi e micosi, disinfetta e aiuta la
                          cicatrizzazione di ferite.
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
                        <v-expansion-panel-header
                          color="blue"
                          class="white--text"
                          >SPA</v-expansion-panel-header
                        ><v-expansion-panel-content
                          class="body-1 pa-2 text-left"
                          style="width:100%"
                        >
                          Idromassaggio che riduce la tensione nervosa ed ha un
                          effetto rilassante, massaggia a fondo la cute e
                          tonifica la muscolatura.
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
                <v-row justify="center" class="pa-3" style="width:100%">
                  <div class="title">
                    Per info e appuntamenti:
                  </div>
                </v-row>
                <v-row justify="center" class="pa-3" style="width:100%">
                  <div class="body-2">
                    <v-icon class="pr-3">mdi-phone</v-icon>
                  </div>
                  <div class="title">
                    <a href="tel:+393491011358">349 1011358</a>
                  </div>
                </v-row>
                <v-row justify="center" class="pa-3" style="width:100%">
                  <div class="body-2">
                    <v-icon class="pr-3" color="orange">mdi-email</v-icon>
                  </div>
                  <div class="title">
                    <a href="mailto:spelacchiodog@gmail.com"
                      >spelacchiodog@gmail.com</a
                    >
                  </div>
                </v-row>
              </v-row>
              <v-row justify="center" style="margin-top:20px">
                <v-avatar class="profile" size="164" tile>
                  <v-img :src="spelacchio" contain></v-img>
                </v-avatar>

                <v-list-item color="rgba(0, 0, 0, .4)" dark>
                  <v-list-item-content>
                    <v-list-item-title class="title"
                      >SPELACCHIO</v-list-item-title
                    >
                  </v-list-item-content>
                </v-list-item>
              </v-row>
            </v-sheet>
          </div>
        </v-flex>
        <!-- <v-fab-transition>
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
    </section>
    <FooterLarge
      class="hidden-sm-and-down"
      :is_toelettatura="is_toelettatura"
    />
  </div>
</template>

<script>
import { Logo, FooterLarge, razor, comb, stripping } from '@/components/'
// import Breadcrumbs from '@/components/Breadcrumbs.vue'
export default {
  name: 'Struttura',
  components: {
    Logo,
    FooterLarge,
    razor,
    comb,
    stripping
    // Breadcrumbs
  },

  data() {
    return {
      show: false,
      background:
        'background:url(' +
        require('@/static/toelettatura-2.jpg') +
        ');background-position:100% 30%;background-size:45%;background-repeat:no-repeat;background-color:white',
      is_toelettatura: true,
      length: 3,
      window: 0,
      style:
        'background: url(' +
        require('@/static/servizi-toelettatura-banner-mobile.jpg') +
        ');' +
        'background-position:center top',
      spelacchio: require('@/static/spelacchio-logo grande.png'),
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
  head() {
    return {
      title: 'Dog Is Good | Toelettatura',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content:
            ' Bellezza e salute del cane sono ciò in cui crediamo, il nostro motto è: "amore, cura e rispetto!" Per info: spelacchiodog@gmail.com, tel: 3491011358'
        }
      ]
    }
  },
  layout: 'homepage'
}
</script>

<style lang="scss">
@import '~/assets/content.scss';
</style>
