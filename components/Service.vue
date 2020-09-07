<template>
  <div style="height:100%">
    <v-simple-table>
      <template v-slot:default>
        <thead>
          <tr id="shape">
            <th class="text-left shape-left">&nbsp;</th>
            <th class="text-right shape-right display-2 font-weight-bold">
              Servizi
            </th>
          </tr>
        </thead>
      </template>
    </v-simple-table>
    <v-container fill-height>
      <v-row id="shape-content" align="stretch" dense justify="space-between">
        <v-col class="shape-content-left" :cols="4"> </v-col>
        <v-col class="shape-content-right" :cols="8"
          ><div class="right_card">
            <Card :service="asilo" :img="asilo.src" :to="asilo.to" nuxt />
            <Card
              :service="toelettatura"
              :img="toelettatura.src"
              nuxt
              :to="toelettatura.to"
            /><Card
              nuxt
              :service="educazione"
              :img="educazione.src"
              :to="educazione.to"
            />
          </div>
          <v-spacer></v-spacer>
          <v-row
            align="center"
            align-content="center"
            justify="center"
            class="mx-auto"
          >
            <v-btn
              raised
              primary
              elevation="7"
              large
              nuxt
              width="500"
              color="primary"
              to="./servizi/"
              >Altri servizi</v-btn
            ></v-row
          >
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import Card from '~/components/Card.vue'
export default {
  name: 'Service',
  components: {
    Card
  },
  data() {
    return {
      toelettatura: {
        name: 'Toelettatura',
        subtitle: 'Toelettatura Dog Is Good by Spelacchio!',
        text:
          'Bellezza e salute del cane sono ciò in cui crediamo, il nostro motto è "amore, cura e rispetto"',
        src: require('@/static/toelettatura-home.jpg'),
        to: './servizi/toelettatura'
      },
      asilo: {
        name: 'Asilo',
        text: "L'asilo per cani Dog Is Good",
        src: require('@/static/struttura.jpg'),
        to: './asilo'
      },
      educazione: {
        name: 'Percorsi Educativi',
        text:
          "Il nostro addestramento è detto 'Gentile', adatto a qualunque cane",
        src: require('@/static/servizi-campo-educazione-privato-banner-mobile.jpg'),
        to: './percorsi/'
      }
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/service.scss';
</style>
