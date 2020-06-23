<template>
  <v-card max-width="85vw" class="mx-auto">
    <v-expansion-panels>
      <v-expansion-panel
        v-for="(card, i) in cards"
        :key="i"
        class="cards-wrapper"
      >
        <v-expansion-panel-header :id="'card-exp-' + card.order" :ripple="true"
          >{{ card.title
          }}<template v-slot:actions :elevation="1">
            <v-icon id="asilo">mdi-home</v-icon>
          </template></v-expansion-panel-header
        >
        <v-expansion-panel-content id="card-content">
          <v-card :raised="true" class="mx-auto" max-width="80vw">
            <v-card-text>
              <div class="text--primary">
                Il nostro cane è un compagno di vita e condivide con noi
                avventure e tempo libero, ma gli impegni quotidiani, spesso, ci
                tengono fuori casa per parecchie ore costringendo il nostro
                amico a rimanere solo e recluso. L’idea del nostro asilo nasce
                proprio da una riflessione intorno alle esigenze di entrambi.
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
    <v-app-bar id="card-1" light>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>DOG IS GOOD | L'ASILO PER CANI</v-toolbar-title>

      <v-spacer></v-spacer>
    </v-app-bar>

    <v-container>
      <v-row dense>
        <v-col cols="12">
          <v-card color="#385F73" dark>
            <v-card-title class="headline">Unlimited music now</v-card-title>

            <v-card-subtitle
              >Listen to your favorite artists and albums whenever and wherever,
              online and offline.</v-card-subtitle
            >

            <v-card-actions>
              <v-btn text>Listen Now</v-btn>
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
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    activeClass: 'cards-wrapper',
    items: [
      {
        color: '#1F7087',
        src: 'https://cdn.vuetifyjs.com/images/cards/foster.jpg',
        title: 'Supermodel',
        artist: 'Foster the People'
      },
      {
        color: '#952175',
        src: 'https://cdn.vuetifyjs.com/images/cards/halcyon.png',
        title: 'Halcyon Days',
        artist: 'Ellie Goulding'
      }
    ],
    cards: [
      {
        title: "Dog is good | L' asilo per cani",
        icon: 'mdi-home',
        order: '1'
      }
    ]
  })
}
</script>

<style lang="scss" scoped>
@import '@/assets/cards.scss';
</style>
