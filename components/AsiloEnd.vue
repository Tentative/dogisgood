<template>
  <div>
    <v-flex>
      <section id="second_content_large" :style="style_2">
        <v-container fluid
          ><v-row
            justify="center"
            align="center"
            style="width:100%;margin-left:auto;margin-right:auto"
          >
            <v-col :cols="6">
              <v-card width="100%" class="pa-5">
                <v-row>
                  <v-col :cols="6">
                    <v-img :src="grid_1" />
                  </v-col>
                  <v-col :cols="6"> <v-img :src="grid_2"/></v-col
                ></v-row>
                <v-row>
                  <v-col :cols="6" style="background-size:cover;">
                    <v-img :src="grid_3" style="height:100%" />
                  </v-col>
                  <v-col :cols="6"> <v-img :src="grid_4"/></v-col
                ></v-row> </v-card
            ></v-col>
            <v-col :cols="6">
              <v-card class="pa-5">
                <v-card-text class="title"
                  >L’asilo è quindi il luogo che può, con competenza e serietà,
                  sostituirsi al suo compagno umano nei momenti di assenza,
                  quando sono necessarie attenzioni particolari sia per i
                  cuccioli, sia per i soggetti molto anziani, o anche
                  semplicemente quando le condizioni atmosferiche non ci
                  consentono lunghe passeggiate.
                </v-card-text>
                <v-card-text class="title"
                  >Affinché tutti i cani possano interagire nella maniera
                  migliore, ogni nostro ospite usufruirà di un’ora di prova
                  gratuita per comprendere se l’asilo è il posto migliore per
                  lui e se necessita eventualmente di un percorso di
                  inserimento.
                </v-card-text></v-card
              >
            </v-col>
          </v-row></v-container
        >
      </section></v-flex
    >
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'AsiloEnd',
      grid_1: require('@/static/struttura3.jpg'),
      grid_2: require('@/static/struttura2.jpg'),
      grid_3: require('@/static/struttura3-bis.jpg'),
      grid_4: require('@/static/servizi-campo-educazione-privato-banner-mobile.jpg')
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/global.scss';
</style>
