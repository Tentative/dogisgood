<template>
  <section id="content_large" :style="style" class="hidden-sm-and-down">
    <v-container style="background-color:rgba(0,0,0,0.6)">
      <v-row id="main_row" justify="center">
        <v-col :cols="12">
          <div
            id="content-title"
            class="  text-center display-4"
            style="color:white"
          >
            I nostri servizi
          </div>
        </v-col>
      </v-row>
      <v-row id="main_row" justify="center">
        <v-col :cols="12">
          <!-- <div class="sub_heading text-center display-3 pa-10">
                Il nostro è il metodo di educazione detto gentile, adatto a
                qualunque cane.
              </div> -->
        </v-col>
      </v-row>
      <v-row id="main_row" justify="center"> </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  layout: 'homepage'
}
</script>
