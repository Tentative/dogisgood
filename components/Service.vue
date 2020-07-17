<template>
  <div>
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

    <v-row id="shape-content">
      <v-col class="shape-content-left" :cols="4"> </v-col>
      <v-col class="shape-content-right" :cols="8"
        ><Card :service="toelettatura"
      /></v-col>
    </v-row>
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
      }
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/service.scss';
</style>
