<template>
  <div>
    <v-flex>
      <section id="content_large" :style="style">
        <v-container style="background-color:rgba(0,0,0,0.4)">
          <v-row id="main_row" justify="center">
            <v-col :cols="12">
              <div
                id="content-title"
                class="  text-center display-4"
                style="color:white"
              >
                L'asilo
              </div>
            </v-col>
          </v-row>
          <v-row id="main_row" justify="center">
            <v-col :cols="12">
              <div class="sub_heading text-center display-3 pa-10">
                Perché un cane educato e stanco è un cane felice, con un
                proprietario sereno e contento.
              </div>
            </v-col>
          </v-row>
          <v-row id="main_row" justify="center">
            <v-col :cols="12">
              <div class=" text-center">
                <v-btn color="blue pa-5">Scopri</v-btn>
                <v-btn color="#aae56d" class=" pa-5 ma-5">Info e costi</v-btn>
              </div>
            </v-col>
          </v-row>
        </v-container>
      </section>
    </v-flex>
  </div>
</template>

<script>
export default {
  name: 'Content',
  data() {
    return {
      asilo1: require('@/static/asilo-1.jpg'),
      style:
        'background:rgba(0,0,0,0.4)url(' +
        require('@/static/asilo-1.jpg') +
        ');background-size:cover;background-position: left center;'
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/content.scss';
</style>
