<template>
  <div id="home">
    <v-card max-width="85vw" class="mx-auto">
      <v-expansion-panels>
        <v-expansion-panel v-for="(card, i) in cards" id="panel-1" :key="i">
          <v-expansion-panel-header
            :id="'card-exp-' + card.order"
            :ripple="true"
            >{{ card.title
            }}<template v-slot:actions :elevation="1">
              <v-icon id="asilo">mdi-home</v-icon>
            </template></v-expansion-panel-header
          >
          <v-expansion-panel-content id="card-content-1">
            <v-card :raised="true" class="mx-auto" max-width="80vw">
              <v-card-text>
                <div class="text--primary">
                  {{ card.content }}
                </div>
              </v-card-text>
              <v-card-actions>
                <v-btn text color="deep-purple accent-4" to="/asilo">
                  Scopri di più
                </v-btn>
              </v-card-actions>
            </v-card>
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </v-card>

    <v-card max-width="85vw" class="mx-auto" style="margin-top:-25px;">
      >
      <v-expansion-panels>
        <v-expansion-panel id="panel-2">
          <v-expansion-panel-header id="card-exp-2" :ripple="true"
            >TOELETTATURA<template v-slot:actions :elevation="1">
              <v-icon id="struttura">mdi-bone</v-icon>
            </template></v-expansion-panel-header
          >
          <v-expansion-panel-content id="card-content">
            <v-img :src="dio" height="200px"></v-img>

            <v-card-title>
              Toelettatura
            </v-card-title>

            <v-card-subtitle>
              by Spelacchio!
            </v-card-subtitle>

            <v-card-actions>
              <v-btn outlined color="purple" text to="/servizi/toelettatura">
                Scopri
              </v-btn>

              <v-spacer></v-spacer>
            </v-card-actions>
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
      <v-card max-width="85vw" class="mx-auto">
        <v-expansion-panels>
          <v-expansion-panel id="panel-3">
            <v-expansion-panel-header id="card-exp-3" :ripple="true"
              >STRUTTURA<template v-slot:actions :elevation="1">
                <v-icon id="percorsi">mdi-paw</v-icon>
              </template></v-expansion-panel-header
            >
            <v-expansion-panel-content id="card-content">
              <v-img :src="imgSrc" height="200px"></v-img>

              <v-card-title>
                La nostra struttura
              </v-card-title>

              <v-card-subtitle>
                Via San Vitale 129 - Seregno (MB)
              </v-card-subtitle>

              <v-card-actions>
                <v-btn
                  text
                  href="https://www.facebook.com/sharer/sharer.php?u=https%3A%2F%2Fwww.facebook.com%2Fasilodogisgood%2F&amp;src=sdkpreparse"
                  >Condividi<v-icon right dark>mdi-share-variant</v-icon></v-btn
                >

                <v-btn outlined color="purple" text to="/struttura">
                  Scopri
                </v-btn>

                <v-spacer></v-spacer>

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
                    La struttura che ospita l’Asilo Dog is Good è stata
                    realizzata per rispondere al meglio a tutte le esigenze dei
                    nostri amici pelosi e offrire comfort, igiene e sicurezza
                    adeguati al loro benessere. 400 mq e un ampio cortile
                    privato a disposizione.
                  </v-card-text>
                </div>
              </v-expand-transition>
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>
      </v-card>
    </v-card>
    <v-card max-width="85vw" class="mx-auto">
      <v-expansion-panels>
        <v-expansion-panel id="panel-4">
          <v-expansion-panel-header id="card-exp-4" :ripple="true"
            >SERVIZI<template v-slot:actions :elevation="1">
              <v-icon id="servizi">mdi-dog</v-icon>
            </template></v-expansion-panel-header
          >
          <v-expansion-panel-content id="card-content-4">
            <v-container fluid>
              <v-row dense>
                <v-col
                  v-for="card in cardsGrid"
                  :key="card.title"
                  :cols="card.flex"
                >
                  <v-card>
                    <v-img
                      :src="card.src"
                      class="white--text align-end"
                      gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                      height="200px"
                    >
                      <v-card-title v-text="card.title"></v-card-title>
                    </v-img>

                    <v-card-actions>
                      <v-spacer></v-spacer>

                      <v-btn outlined color="purple" text :to="card.to">
                        Scopri
                      </v-btn>
                    </v-card-actions>
                  </v-card>
                </v-col>
              </v-row>
            </v-container>
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </v-card>
    <div id="partners" class="text-center mx-auto title">
      I nostri partner:
    </div>

    <v-row justify="center" class="mx-auto mt-3">
      <v-carousel
        cycle
        height="200"
        width="85vw"
        hide-delimiter-background
        show-arrows
        interval="3000"
      >
        <v-row class="mx-auto" justify="center">
          <v-carousel-item
            v-for="partner in partners"
            :key="partner"
            :href="partner.to"
            class="mx-auto"
          >
            <v-img
              :src="partner.icon"
              width="30vw"
              height="auto"
              class="text-center mx-auto"
            />
            <div class="title text-center black--text">
              {{ partner.title }}
            </div>
          </v-carousel-item>
        </v-row>
      </v-carousel>
    </v-row>
    <div id="partners" class="text-center mx-auto title">
      Seguici sui nostri social
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    logoSrc: require('@/static/logo.jpg'),
    show: false,
    text: 'i nostri partner:',
    imgSrc: require('@/static/struttura.jpg'),
    partnerSrc: require('@/static/feste-di-compleanno.jpg'),
    cardSrc: require('@/static/puppy-school.jpg'),
    icons: ['mdi-phone', 'mdi-email', 'mdi-whatsapp', 'mdi-facebook'],
    dio: require('@/static/toelettatura-home.jpg'),
    cardsGrid: [
      {
        title: 'Percorsi educativi',
        src: require('@/static/percorsi-puppy-school-banner-mobile.jpg'),
        flex: 12,
        to: 'percorsi/'
      },
      {
        title: 'Bautique',
        src: require('@/static/bautique.jpg'),
        flex: 6,
        to: 'servizi/bautique'
      },
      {
        title: 'Wedding dog sitter',
        src: require('@/static/wedding1.jpg'),
        flex: 6,
        to: 'servizi/wedding-dog-sitter'
      },
      {
        title: 'Feste di compleanno',
        src: require('@/static/compleanno-home.jpg'),
        flex: 6,
        to: 'servizi/compleanno'
      },
      {
        title: 'Osteopatia animale',
        src: require('@/static/osteopatia-home.jpg'),
        flex: 6,
        to: 'servizi/osteopatia'
      },
      {
        title: 'Campo di educazione privato',
        src: require('@/static/camp2.JPG'),
        flex: 12,
        to: 'servizi/campo-educazione-privato'
      }
    ],
    toelettatura: [
      {
        title: 'Toelettatura',
        src: require('@/static/toelettatura-home.jpg'),
        flex: 12,
        to: 'servizi/toelettatura'
      }
    ],
    partners: [
      {
        icon: require('@/static/partners/gammavet.png'),
        title: 'Gammavet',
        to: 'http://www.gammavet.it/'
      },
      {
        icon: require('@/static/partners/lussianinda.png'),
        title: 'Lussianinda',
        to: 'https://shop.lussianinda.com/'
      },
      {
        icon: require('@/static/partners/mariani.png'),
        title: 'Ilaria Mariani CRF',
        to: 'https://ilariamarianicrf.com/'
      }
    ],
    items: [
      {
        color: '#f59242',
        src: require('@/static/puppy-school.jpg'),
        title: 'Puppy school',
        artist: 'Obiettivi: benessere di cucciolo e proprietario',
        button: 'Scopri',
        to: '/percorsi/puppy-school'
      },
      {
        color: '#f542a5',
        src: require('@/static/percorsi-personalizzati.jpg'),
        title: 'Percorsi su misura',
        artist:
          'Per ulteriori informazioni ed iscrizioni non esitate a contattarci.',
        button: 'Contattaci'
      }
    ],
    cards: [
      {
        title: "L' asilo per cani",
        icon: 'mdi-home',
        order: '1',
        content:
          'Il nostro cane è un compagno di vita e condivide con noi avventure e tempo libero, ma gli impegni quotidiani, spesso, ci tengono fuori casa per parecchie ore costringendo il nostro amico a rimanere solo e recluso. L’idea del nostro asilo nasce proprio da una riflessione intorno alle esigenze di entrambi.'
      }
    ]
  })
}
</script>

<style lang="scss" scoped>
@import '@/assets/cards.scss';
</style>
