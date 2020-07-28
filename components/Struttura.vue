<template>
  <div>
    <v-sheet id="struttura" color="rgba(0,0,0,0)">
      <v-sheet class="intro_struttura title" color="#aae56d" light>
        La struttura che ospita l’Asilo Dog is Good è stata realizzata per
        rispondere al meglio a tutte le esigenze dei nostri amici pelosi e
        offrire comfort, igiene e sicurezza adeguati al loro benessere. 400 mq e
        un ampio cortile privato a disposizione.
        <!-- <p style="text-align:center">
          <v-btn depressed large color="primary" to="/struttura">Info</v-btn>
        </p> -->
      </v-sheet>
    </v-sheet>
  </div>
</template>

<script>
export default {
  name: 'Struttura'
}
</script>

<style lang="scss" scoped>
@import '@/assets/struttura.scss';
</style>
