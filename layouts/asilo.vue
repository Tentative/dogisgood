<template>
  <div id="content_desktop">
    <v-simple-table>
      <template v-slot:default>
        <thead>
          <tr id="shape">
            <th class="text-left shape-left_large">&nbsp;</th>
            <th class="text-left shape-right_large">Asilo</th>
            <th class="logo_menu">
              <v-img id="logo_right" :src="logo_right" />
            </th>
          </tr>
        </thead>
      </template>
    </v-simple-table>
    <v-container>
      <v-row id="shape-content" align="stretch" dense>
        <v-col class="shape-content-left" :cols="4"
          ><div class="text-center">
            <v-sheet
              id="main-content-desktop"
              color="white"
              style="margin-bottom:20px"
              >Il nostro cane è un compagno di vita e condivide con noi
              avventure e tempo libero, ma gli impegni quotidiani, spesso, ci
              tengono fuori casa per parecchie ore costringendo il nostro amico
              a rimanere solo e recluso.<br /><br />
              L’idea del nostro asilo nasce proprio da una riflessione intorno
              alle esigenze di entrambi. L’asilo è lo spazio dove il nostro cane
              può giocare, correre, riposarsi, uscire nel nostro cortile privato
              e fare tante attività nel nostro grande campo di educazione.
              <br />
              <br />Può vivere quindi nel migliore dei modi quella esperienza di
              socializzazione fondamentale per il suo benessere psicofisico,
              sempre sotto la sorveglianza attenta frutto dei nostri studi di
              educazione cinofila. Perché un cane educato e stanco è un cane
              felice, con un proprietario sereno e contento. L’asilo è quindi il
              luogo che può, con competenza e serietà, sostituirsi al suo
              compagno umano nei momenti di assenza, quando sono necessarie
              attenzioni particolari sia per i cuccioli, sia per i soggetti
              molto anziani, o anche semplicemente quando le condizioni
              atmosferiche non ci consentono lunghe passeggiate. Affinché tutti
              i cani possano interagire nella maniera migliore, ogni nostro
              ospite usufruirà di un’ora di prova gratuita per comprendere se
              l’asilo è il posto migliore per lui e se necessita eventualmente
              di un percorso di inserimento.
            </v-sheet>
            <v-spacer></v-spacer>
          </div>
        </v-col>
        <v-col class="shape-content-right" :cols="8"
          ><v-row>
            <v-col :cols="6"> </v-col>
            <v-col :cols="6"
              ><div class="media1">
                <v-img :src="asilo1" />
              </div>
            </v-col>
          </v-row>
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
export default {
  data() {
    return {
      asilo1: require('@/static/asilo-1.jpg'),
      logo_right: require('@/static/logo-circle.png')
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/service.scss';
@import '@/assets/content.scss';
</style>
