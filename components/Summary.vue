<template>
  <v-container style="margin-top:20px">
    <v-row justify="center" style="width: 100%" class="mx-auto pa-8">
      <v-col :cols="4">
        <v-row
          justify="center"
          class="mx-auto"
          style="margin-left:auto;margin-rigth:auto"
        >
          <v-row justify="center" style="width:100%">
            <v-icon size="62" color="blue">mdi-home</v-icon>
          </v-row>
          <v-row justify="center" style="width:100%;padding:25px">
            <v-sheet class="title"
              >Il nostro cane è un compagno di vita e condivide con noi
              avventure e tempo libero, ma gli impegni quotidiani, spesso, ci
              tengono fuori casa per parecchie ore costringendo il nostro amico
              a rimanere solo e recluso.
            </v-sheet>
          </v-row>
        </v-row>
      </v-col>
      <v-col :cols="4">
        <v-row
          justify="center"
          class="mx-auto"
          style="margin-left:auto;margin-rigth:auto"
        >
          <v-row justify="center" style="width:100%">
            <v-icon size="62" color="blue">mdi-paw</v-icon>
          </v-row>
          <v-row justify="center" style="width:100%;padding:25px">
            <v-sheet class="title">
              L’idea del nostro asilo nasce proprio da una riflessione intorno
              alle esigenze di entrambi. L’asilo è lo spazio dove il nostro cane
              può giocare, correre, riposarsi, uscire nel nostro cortile privato
              e fare tante attività nel nostro grande campo di educazione.
            </v-sheet>
          </v-row>
        </v-row>
      </v-col>
      <v-col :cols="4">
        <v-row
          justify="center"
          class="mx-auto"
          style="margin-left:auto;margin-rigth:auto"
        >
          <v-row justify="center" style="width:100%">
            <v-icon size="62" color="blue">mdi-bone</v-icon>
          </v-row>
          <v-row justify="center" style="width:100%;padding:25px">
            <v-sheet class="title"
              >Può vivere quindi nel migliore dei modi quella esperienza di
              socializzazione fondamentale per il suo benessere psicofisico,
              sempre sotto la sorveglianza attenta frutto dei nostri studi di
              educazione cinofila.
            </v-sheet>
          </v-row>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      name: 'Summary'
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/content.scss';
</style>
