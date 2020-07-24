<template>
  <section id="costi" style="margin-top:20px">
    <v-container>
      <v-row class="mx-auto" justify="center">
        <div
          class="display-2 text-xs-subheading text-center blue--text text-uppercase mt-5 font-weight-bold"
          style="width:100%"
        >
          I nostri prezzi
        </div>
        <div
          class="text-center headline text-uppercase font-weight-bold mt-5"
          style="color:#aae56d;margin-left:auto;margin-right:auto"
        >
          Percorsi di educazione personalizzati per cuccioli e adulti
        </div>
      </v-row>
      <v-row
        justify="center"
        style="width:100%;margin-left:auto;margin-right:auto"
      >
        <v-simple-table id="table">
          <template v-slot:default>
            <thead>
              <tr>
                <th
                  class="text-center headline text-uppercase font-weight-bold"
                  style="color:#aae56d;margin-left:auto;margin-right:auto"
                ></th>
                <th class="text-left"></th>
              </tr>
            </thead>
            <tbody id="stripe" style="margin-top:20px">
              <tr v-for="service in services" :key="service.name">
                <td class="title">{{ service.name }}</td>
                <td class="title">{{ service.prezzo }}</td>
              </tr>
            </tbody>
          </template>
        </v-simple-table>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'Costi',
  data() {
    return {
      services: [
        {
          name: '1 Lezione 1 Ora',
          prezzo: '€ 45'
        },
        {
          name: 'Pacchetto 8 lezioni',
          prezzo: '€ 320'
        },
        {
          name: 'Puppy School (6 lezioni + 3 ingressi mezza giornata)',
          prezzo: '€ 270'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/costi.scss';
</style>
