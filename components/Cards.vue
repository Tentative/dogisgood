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
              <v-layout id="top" column justify-center align-center>
                <v-flex xs12 class="main-banner">
                  <Logo />
                  <div id="content-title" class="title text-center">
                    Percorsi educativi
                  </div>
                  <div class="text-center">
                    <v-sheet id="main-content" color="white"
                      >Il nostro è il metodo di educazione detto gentile, adatto
                      a qualunque cane, indipendentemente da razza, età, sesso e
                      caratteristiche individuali, e personalizzato con uno
                      studio attento dell’animale affinché possa offrire la
                      massima efficacia. Durante un percorso di educazione, cane
                      e proprietario imparano, insieme, gli esercizi di base
                      utili nella vita quotidiana, come la condotta al
                      guinzaglio e il richiamo, ma soprattutto a relazionarsi
                      nel migliore dei modi, a risolvere piccoli e grandi
                      problemi ed avere così una vita insieme più felice e
                      semplice per entrambi.
                    </v-sheet>
                    <div class="media1">
                      <v-img :src="asilo1" />
                    </div>
                    <v-card
                      id="percorsi-card"
                      class="mx-auto"
                      width="85vw"
                      color="#26c6da"
                      dark
                      style="margin-bottom: 20px"
                    >
                      <v-card-title>
                        <v-icon large left>
                          mdi-paw
                        </v-icon>
                        <span class="title font-weight-light"
                          >Puppy School</span
                        >
                      </v-card-title>

                      <v-card-text class="headline font-weight-bold">
                        Gli obiettivi di questo percorso sono diversi e
                        contribuiscono tutti al benessere di cucciolo e
                        proprietario e alla crescita serena del nostro piccolo
                        amico.
                      </v-card-text>

                      <v-card-actions>
                        <v-list-item class="grow">
                          <v-list-item-avatar color="grey darken-3">
                            <v-img class="elevation-6" :src="logoSrc"></v-img>
                          </v-list-item-avatar>

                          <v-list-item-content>
                            <v-list-item-title></v-list-item-title>
                          </v-list-item-content>

                          <v-row align="center" justify="end">
                            <v-btn
                              outlined
                              color="purple"
                              text
                              to="./puppy-school"
                            >
                              Scopri
                            </v-btn>
                          </v-row>
                        </v-list-item>
                      </v-card-actions>
                    </v-card>
                    <v-sheet id="main-content" color="white"
                      >Se invece sei alla ricerca del tuo amico peloso, ti
                      offriamo la migliore consulenza, competente e attenta, che
                      ti guidi in un percorso di adozione maturo e responsabile.
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

    <v-carousel
      height="40px"
      cycle
      hide-delimiter-background
      show-arrows-on-hover
      style="margin-top:20px"
    >
      <v-carousel-item v-for="n in 3" :key="n">
        <v-row justify="space-around">
          <v-avatar color="indigo" size="28">
            <v-icon dark>mdi-account-circle</v-icon>
          </v-avatar>

          <v-avatar color="indigo" size="28">
            <v-icon dark>mdi-account-circle</v-icon>
          </v-avatar>

          <v-avatar color="indigo" size="28">
            <v-icon dark>mdi-account-circle</v-icon>
          </v-avatar>
        </v-row>
      </v-carousel-item>
    </v-carousel>
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
    cardsGrid: [
      {
        title: 'Toelettatura',
        src: require('@/static/toelettatura-home.jpg'),
        flex: 12,
        to: 'servizi/toelettatura'
      },
      {
        title: 'Bautique',
        src: require('@/static/bautique.jpg'),
        flex: 6,
        to: 'servizi/bautique'
      },
      {
        title: 'Wedding dog sitter',
        src: require('@/static/wedding-dog-sitter.jpg'),
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
        src: require('@/static/campo-addestramento-privato.jpg'),
        flex: 12,
        to: 'servizi/campo-educazione-privato'
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

<style lang="scss">
@import '@/assets/cards.scss';
</style>
