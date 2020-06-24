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
    <v-card class="mx-auto" max-width="85vw">
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
  </div>
</template>

<script>
export default {
  data: () => ({
    show: false,
    imgSrc: require('@/static/struttura.jpg'),
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
