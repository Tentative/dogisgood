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
          <v-expansion-panel-content id="card-content">
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
            <v-img
              src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
              height="200px"
            ></v-img>

            <v-card-title>
              Top western road trips
            </v-card-title>

            <v-card-subtitle>
              1,000 miles of wonder
            </v-card-subtitle>

            <v-card-actions>
              <v-btn text>Share</v-btn>

              <v-btn color="purple" text>
                Explore
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
                  I'm a thing. But, like most politicians, he promised more than
                  he could deliver. You won't have time for sleeping, soldier,
                  not with all the bed making you'll be doing. Then we'll go
                  with that data file! Hey, you add a one and two zeros to that
                  or we walk! You're going to do his laundry? I've got to find a
                  way to escape.
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
