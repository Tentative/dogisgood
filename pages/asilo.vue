<template>
  <div>
    <v-layout
      id="top"
      style="max-width:100%!important"
      column
      justify-center
      align-center
    >
      <v-flex xs12 class="main-banner">
        <Logo
          class="d-md-none"
          :src="asilo_src"
          :content="asilo_content"
          :title="asilo_title"
          :intro="asilo_intro"
          :sub="asilo_sub"
        />
        <Content class="hidden-sm-and-down d-sm-none d-md-flex" />
        <Summary class="hidden-sm-and-down d-sm-none d-md-flex" />
        <AsiloEnd class="hidden-sm-and-down d-sm-none d-md-flex" />
        <Costi class="hidden-sm-and-down d-sm-none d-md-flex" />

        <v-container id="mobile" class="d-md-none d-lg-none d-xl-none">
          <div id="content-title" class="title text-center text-xs-body-2">
            L'asilo
          </div>
          <v-row justify="center" style="margin-left:auto;margin-right:auto">
            <v-col xs="12" sm="12" md="7">
              <div class="text-left">
                <v-sheet
                  id="main-content"
                  color="white"
                  style="margin-bottom:20px"
                  >Il nostro cane è un compagno di vita e condivide con noi
                  avventure e tempo libero, ma gli impegni quotidiani, spesso,
                  ci tengono fuori casa per parecchie ore costringendo il nostro
                  amico a rimanere solo e recluso.<br /><br />
                  L’idea del nostro asilo nasce proprio da una riflessione
                  intorno alle esigenze di entrambi.<br />
                  L’asilo è lo spazio dove il nostro cane può giocare, correre,
                  riposarsi, uscire nel nostro cortile privato e fare tante
                  attività nel nostro grande campo di educazione.
                </v-sheet>
                <v-img
                  :src="asilo2"
                  width="85vw"
                  style="border-radius:10px;margin-bottom:20px"
                  class="mx-auto"
                />

                <v-sheet id="content" color="white">
                  Può vivere quindi nel migliore dei modi quella esperienza di
                  socializzazione fondamentale per il suo benessere psicofisico,
                  sempre sotto la sorveglianza attenta frutto dei nostri studi
                  di educazione cinofila.<br /><br />
                  Perché un cane <strong>educato</strong> e
                  <strong>stanco</strong> è un cane
                  <span class="primary--text">felice</span>, con un proprietario
                  <strong>sereno</strong> e <strong>contento</strong>.<br />
                  <br />
                  L’asilo è quindi il luogo che può, con competenza e serietà,
                  sostituirsi al suo compagno umano nei momenti di assenza,
                  quando sono necessarie attenzioni particolari sia per i
                  cuccioli, sia per i soggetti molto anziani, o anche
                  semplicemente quando le condizioni atmosferiche non ci
                  consentono lunghe passeggiate.<br /><br />
                  Affinché tutti i cani possano interagire nella maniera
                  migliore, ogni nostro ospite usufruirà di un’ora di prova
                  gratuita per comprendere se l’asilo è il posto migliore per
                  lui e se necessita eventualmente di un percorso di
                  inserimento.
                </v-sheet>
              </div>
              <Costi class="d-xs-flex d-sm-flex d-md-hide" />
            </v-col>

            <v-carousel
              cycle
              height="250"
              hide-delimiter-background
              show-arrows-on-hover
              class="d-md-none"
              ><v-carousel-item
                v-for="(slide, i) in slides"
                :key="i"
                class="pa-5"
                ><v-img :src="slide.src"/></v-carousel-item
            ></v-carousel>
          </v-row>
        </v-container>
        <div id="content-title" class="text-center title text-xs-body-2">
          Il nostro asilo è aperto
        </div>
        <div
          id="content-title"
          class="text-center title text-xs-body-2 hidden-sm-and-down"
          style="margin-bottom:20px"
        >
          dal lunedì al venerdì, dalle 7.30 alle 19
        </div>
        <div
          id="content-title"
          class="text-center title text-xs-body-2 hidden-sm-and-down"
          style="margin-bottom:20px"
        >
          sabato dalle 9 alle 18
        </div>
        <div
          id="content-title"
          class="text-center title  hidden-md-and-up"
          style="margin-bottom:20px"
        >
          dal lunedì al venerdì, dalle 7.30 alle 19
        </div>
        <div
          id="content-title"
          class="text-center title  hidden-md-and-up"
          style="margin-bottom:20px"
        >
          sabato dalle 9 alle 18
        </div>
      </v-flex>

      <!-- <Breadcrumbs :levels="1" /> -->
    </v-layout>
    <FooterLarge class="hidden-sm-and-down" />
  </div>
</template>

<script>
import {
  Logo,
  Content,
  Summary,
  AsiloEnd,
  Costi,
  FooterLarge
} from '@/components/'
// import Breadcrumbs from '@/components/Breadcrumbs.vue'
export default {
  name: 'Asilo',
  components: {
    Logo,
    Content,
    Summary,
    AsiloEnd,
    Costi,
    FooterLarge
    // Breadcrumbs
  },

  data() {
    return {
      imgSrc: this.$route.name,
      asilo_src: require('@/static/asilo-1.jpg'),
      asilo_content:
        "L'asilo è lo spazio dove il nostro cane può giocare, correre, riposarsi, uscire nel nostro cortile privato e fare tante attività nel nostro grande campo di educazione.",
      fab: false,
      asilo_title: 'Asilo',
      offsetTop: 0,
      asilo1: require('@/static/asilo-1.jpg'),
      asilo_intro: "L'asilo",
      asilo2: require('@/static/asilo-2.jpg'),
      asilo_sub:
        'Il nostro cane è un compagno di vita e condivide con noi avventure e tempo libero, ma gli impegni quotidiani, spesso, ci tengono fuori casa per parecchie ore costringendo il nostro amico a rimanere solo e recluso. L’idea del nostro asilo nasce proprio da una riflessione intorno alle esigenze di entrambi. Può vivere quindi nel migliore dei modi quella esperienza di socializzazione fondamentale per il suo benessere psicofisico, sempre sotto la sorveglianza attenta frutto dei nostri studi di educazione cinofila. Perché un cane educato e stanco è un cane felice, con un proprietario sereno e contento. L’asilo è quindi il luogo che può, con competenza e serietà, sostituirsi al suo compagno umano nei momenti di assenza, quando sono necessarie attenzioni particolari sia per i cuccioli, sia per i soggetti molto anziani, o anche semplicemente quando le condizioni atmosferiche non ci consentono lunghe passeggiate. Affinché tutti i cani possano interagire nella maniera migliore, ogni nostro ospite usufruirà di un’ora di prova gratuita per comprendere se l’asilo è il posto migliore per lui e se necessita eventualmente di un percorso di inserimento. ',
      slides: [
        {
          src: require('@/static/struttura3.jpg')
        },
        {
          src: require('@/static/struttura2.jpg')
        },
        {
          src: require('@/static/struttura5.jpg')
        },
        {
          src: require('@/static/servizi-campo-educazione-privato-banner-mobile.jpg')
        }
      ]
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
      title: 'Dog Is Good | L' + 'asilo',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content:
            'L’asilo è lo spazio dove il nostro cane può fare tante attività nel nostro grande campo di educazione. Perché un cane educato e stanco è un cane felice, con un compagno umano sereno e contento!'
        }
      ]
    }
  },
  layout: 'homepage'
}
</script>

<style lang="scss" scoped>
@import '~/assets/content.scss';
</style>
