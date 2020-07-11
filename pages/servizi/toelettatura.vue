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
          >Servizi offerti:
          <v-sheet id="sub-content" dark color="#42a5f5" class="text-center"
            >Bagno di igiene</v-sheet
          >

          <v-sheet id="sub-content" dark color="#42a5f5" class="text-center"
            >Taglio a forbice</v-sheet
          >

          <v-sheet id="sub-content" dark color="#42a5f5" class="text-center"
            >Tosatura</v-sheet
          >

          <v-sheet id="sub-content" dark color="#42a5f5" class="text-center"
            >Snodatura</v-sheet
          >

          <v-sheet id="sub-content" dark color="#42a5f5" class="text-center"
            >Stripping</v-sheet
          >

          <v-sheet id="sub-content" dark color="#42a5f5" class="text-center"
            >Pulizia orecchie e taglio unghie</v-sheet
          >

          <v-sheet id="sub-content" dark color="#42a5f5" class="text-center"
            >Cromoterapia</v-sheet
          >

          <v-sheet id="sub-content" dark color="#42a5f5" class="text-center"
            >Taglio a forbice</v-sheet
          >

          <v-sheet id="sub-content" dark color="#42a5f5" class="text-center">
            Toelettatura sanitaria gatti</v-sheet
          >

          <v-card class="mx-auto" max-width="85vw" style="margin-bottom:20px">
            <v-img :src="bagno" height="100px"></v-img>
            <v-card-title class=" text-center">
              Bagno con acqua ozonizzata
            </v-card-title>

            <v-card-actions>
              <v-btn icon @click="show = !show">
                <v-icon>{{
                  show ? 'mdi-chevron-up' : 'mdi-chevron-down'
                }}</v-icon>
              </v-btn>
            </v-card-actions>
            <v-expand-transition>
              <div v-show="show">
                <v-divider></v-divider>

                <v-card-text>
                  Dona lucentezza, apre i nodi, elimina zecche e pulci, efficace
                  contro dermatosi e micosi, disinfetta e aiuta la
                  cicatrizzazione di ferite.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>

          <v-card class="mx-auto" max-width="85vw" style="margin-bottom:20px">
            <v-img :src="spa" height="100px"></v-img>
            <v-card-title class="text-center card-title">
              <span style="text-align:center">SPA</span>
            </v-card-title>

            <v-card-actions>
              <v-btn icon @click="showspa = !showspa">
                <v-icon>{{
                  showspa ? 'mdi-chevron-up' : 'mdi-chevron-down'
                }}</v-icon>
              </v-btn>
            </v-card-actions>
            <v-expand-transition>
              <div v-show="showspa">
                <v-divider></v-divider>

                <v-card-text>
                  Con idromassaggio che riduce la tensione nervosa ed ha un
                  effetto rilassante , massaggia a fondo la cute e tonifica la
                  muscolatura.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
          Bellezza e salute del cane sono ciò in cui crediamo, il nostro motto è
          "amore, cura e rispetto!"
          <div class="title text-center" style="margin-top:20px">
            Venite a trovarci!
          </div>
          <div class="subtitle-2 text-center">
            <p>Per info e appuntamenti:</p>

            <v-btn icon href="mailto:spelacchiodog@gmail.com">
              spelacchiodog@gmail.com</v-btn
            >
          </div>
          <div class="subtitle-2 text-center">
            <v-btn icon href="tel:393491011358"> 3491011358</v-btn>
          </div>
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
      showspa: false,
      imgSrc: 'struttura',
      fab: false,
      offsetTop: 0,
      bagno: require('@/static/bagno-ozonizzante.jpg'),
      spa: require('@/static/spa.jpg')
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
