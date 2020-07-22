<template>
  <div style="height:100%">
    <v-simple-table>
      <template v-slot:default>
        <thead>
          <tr id="shape">
            <th class="text-left shape-left">&nbsp;</th>
            <th class="text-right shape-right">Servizi</th>
          </tr>
        </thead>
      </template>
    </v-simple-table>
    <v-container fill-height>
      <v-row id="shape-content" align="stretch" dense justify="space-between">
        <v-col class="shape-content-left" :cols="4"> </v-col>
        <v-col class="shape-content-right" :cols="8"
          ><div class="right_card">
            <Card :service="toelettatura" :img="toelettatura.src" /><Card
              :service="asilo"
              :img="asilo.src"
            /><Card :service="educazione" :img="educazione.src" />
          </div>
          <v-spacer></v-spacer>
          <v-row align="center" align-content="center" justify="center">
            <v-btn depressed large color="primary"
              >Vieni a scoprire tutti i nostri servizi!</v-btn
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
        src: require('@/static/toelettatura-home.jpg')
      },
      asilo: {
        name: 'Asilo',
        text: "L'asilo per cani Dog Is Good",
        src: require('@/static/struttura.jpg')
      },
      educazione: {
        name: 'Percorsi Educativi',
        text:
          "Il nostro addestramento è detto 'Gentile', adatto a qualunque cane",
        src: require('@/static/servizi-campo-educazione-privato-banner-mobile.jpg')
      }
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/service.scss';
</style>
