<template>
  <section id="costi">
    <v-container>
      <v-row class="mx-auto" justify="center">
        <div
          class="display-3 text-xs-subheading text-center blue--text text-uppercase hidden-sm-and-down mt-5 pt-5"
        >
          I nostri prezzi
        </div>
        <div
          id="content-title"
          class="title text-center text-xs-body-2 hidden-md-and-up mt-5 pt-5"
        >
          I nostri prezzi
        </div>
      </v-row>
      <v-row
        justify="center"
        style="width:100%;margin-left:auto;margin-right:auto"
      >
        <v-simple-table id="table">
          <template v-slot:default>
            <!-- <thead>
              <tr>
                 <th class="text-left body-2">Asilo</th> 
                <th class="text-left"></th>
              </tr>
            </thead -->
            <tbody id="stripe">
              <tr v-for="service in services" :key="service.name">
                <td>{{ service.name }}</td>
                <td style="width:30%;text-align:right">{{ service.prezzo }}</td>
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
          name: 'INGRESSO UNA GIORNATA',
          prezzo: '€ 28'
        },
        {
          name: 'INGRESSO MEZZA GIORNATA (max 5 ore)',
          prezzo: '€ 23'
        },
        {
          name: 'CARNET 5 INGRESSI GIORNATA INTERA (validità 2 mesi)',
          prezzo: '€ 125'
        },
        {
          name: 'CARNET 5 INGRESSI MEZZA GIORNATA (validità 2 mesi)',
          prezzo: '€ 100'
        },
        {
          name: 'CARNET 10 INGRESSI GIORNATA INTERA (validità 4 mesi)',
          prezzo: '€ 230'
        },
        {
          name: 'CARNET 10 INGRESSI MEZZA GIORNATA (validità 4 mesi)',
          prezzo: '€ 180'
        },
        {
          name: 'ABBONAMENTO MENSILE GIORNATA INTERA',
          prezzo: '€ 390'
        },
        {
          name: 'ABBONAMENTO MENSILE MEZZA GIORNATA',
          prezzo: '€ 300'
        },
        {
          name: 'ORA EXTRA',
          prezzo: '€ 10'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/costi.scss';
</style>
