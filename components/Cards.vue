<template>
  <div>
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
                <v-btn text color="deep-purple accent-4">
                  Scopri di più
                </v-btn>
              </v-card-actions>
            </v-card>
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </v-card>
    <v-card max-width="85vw" class="mx-auto">
      <v-expansion-panels>
        <v-expansion-panel id="panel-2">
          <v-expansion-panel-header id="card-exp-2" :ripple="true"
            >STRUTTURA<template v-slot:actions :elevation="1">
              <v-icon id="struttura">mdi-paw</v-icon>
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

              <v-btn outlined color="purple" text>
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
                  La struttura che ospita l’Asilo Dog is Good è stata realizzata
                  per rispondere al meglio a tutte le esigenze dei nostri amici
                  pelosi e offrire comfort, igiene e sicurezza adeguati al loro
                  benessere. 400 mq e un ampio cortile privato a disposizione.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </v-card>
    <v-card max-width="85vw" class="mx-auto" style="margin-top:-25px;">
      >
      <v-expansion-panels>
        <v-expansion-panel id="panel-3">
          <v-expansion-panel-header id="card-exp-3" :ripple="true"
            >PERCORSI EDUCATIVI<template v-slot:actions :elevation="1">
              <v-icon id="percorsi">mdi-bone</v-icon>
            </template></v-expansion-panel-header
          >
          <v-expansion-panel-content id="card-content-3">
            <v-container>
              <v-row dense>
                <v-col cols="12">
                  <v-card color="#21f37e" light>
                    <v-card-title class="headline"
                      >I nostri percorsi</v-card-title
                    >

                    <v-card-subtitle
                      >Il nostro è il metodo di educazione detto gentile, adatto
                      a qualunque cane</v-card-subtitle
                    >

                    <v-card-actions>
                      <v-btn text>Scopri</v-btn>
                    </v-card-actions>
                  </v-card>
                </v-col>

                <v-col v-for="(item, i) in items" :key="i" cols="12">
                  <v-card :color="item.color" dark>
                    <div class="d-flex flex-no-wrap justify-space-between">
                      <div>
                        <v-card-title
                          class="headline"
                          v-text="item.title"
                        ></v-card-title>

                        <v-card-subtitle v-text="item.artist"></v-card-subtitle>
                      </div>

                      <v-avatar class="ma-3" size="125" tile>
                        <v-img :src="item.src"></v-img>
                      </v-avatar>
                    </div>
                    <v-btn :block="true">{{ item.button }}</v-btn>
                  </v-card>
                </v-col>
              </v-row>
            </v-container>
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </v-card>
    <v-card max-width="85vw" class="mx-auto">
      <v-expansion-panels>
        <v-expansion-panel id="panel-4">
          <v-expansion-panel-header id="card-exp-4" :ripple="true"
            >SERVIZI<template v-slot:actions :elevation="1">
              <v-icon id="percorsi">mdi-dog</v-icon>
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

                      <v-btn icon>
                        <v-icon>mdi-share-variant</v-icon>
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
    <div id="partners" class="text-center mx-auto">
      <v-sheet color="#a5f542" class="title ">I nostri partner:</v-sheet>
    </div>
    <v-carousel
      cycle
      height="250"
      hide-delimiter-background
      show-arrows-on-hover
    >
      <v-carousel-item v-for="n in 3" :key="n">
        <v-card class="mx-auto" max-width="85vw" tile>
          <v-img
            height="100%"
            src="https://cdn.vuetifyjs.com/images/cards/server-room.jpg"
          >
            <v-row align="end" class="fill-height">
              <v-col align-self="start" class="pa-0" cols="12">
                <v-avatar class="profile" color="grey" size="164" tile>
                  <v-img
                    src="https://cdn.vuetifyjs.com/images/profiles/marcus.jpg"
                  ></v-img>
                </v-avatar>
              </v-col>
              <v-col class="py-0">
                <v-list-item color="rgba(0, 0, 0, .4)" dark>
                  <v-list-item-content>
                    <v-list-item-title class="title "
                      >Dog is good</v-list-item-title
                    >
                    <v-list-item-subtitle class="subtitle "
                      >Asilo per cani</v-list-item-subtitle
                    >
                  </v-list-item-content>
                </v-list-item>
              </v-col>
            </v-row>
          </v-img>
        </v-card>
      </v-carousel-item>
    </v-carousel>
    <div id="partners" class="text-center mx-auto">
      <v-sheet color="#a5f542" class="title">Contattaci:</v-sheet>
    </div>
    <v-card flat tile width="85vw%" shaped class="orange lighten-1 text-center">
      <v-card-text>
        <v-btn v-for="icon in icons" :key="icon" class="mx-4" icon>
          <v-icon size="24px">{{ icon }}</v-icon>
        </v-btn>
      </v-card-text>
    </v-card>
  </div>
</template>

<script>
export default {
  data: () => ({
    show: false,
    text: 'i nostri partner:',
    imgSrc: require('@/static/struttura.jpg'),
    partnerSrc: require('@/static/feste-di-compleanno.jpg'),
    cardSrc: require('@/static/puppy-school.jpg'),
    icons: ['mdi-phone', 'mdi-email', 'mdi-whatsapp', 'mdi-facebook'],
    cardsGrid: [
      {
        title: 'Toelettatura',
        src: require('@/static/toelettatura.jpg'),
        flex: 12
      },
      { title: 'Bautique', src: require('@/static/pet-shop.jpg'), flex: 6 },
      {
        title: 'Wedding dog sitter',
        src: require('@/static/wedding-dog-sitter.jpg'),
        flex: 6
      },
      {
        title: 'Feste di compleanno',
        src: require('@/static/feste-di-compleanno.jpg'),
        flex: 6
      },
      {
        title: 'Osteopatia animale',
        src: require('@/static/osteopatia-animale.jpg'),
        flex: 6
      },
      {
        title: 'Campo di educazione privato',
        src: require('@/static/campo-addestramento-privato.jpg'),
        flex: 12
      }
    ],
    items: [
      {
        color: '#f59242',
        src: require('@/static/puppy-school.jpg'),
        title: 'Puppy school',
        artist: 'Obiettivi: benessere di cucciolo e proprietario',
        button: 'Scopri'
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
        title: "Dog is good | L' asilo per cani",
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
