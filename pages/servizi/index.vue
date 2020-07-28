<template>
  <div>
    <section id="content_large" :style="style" class="hidden-sm-and-down">
      <v-container style="background-color:#aae56d">
        <v-row id="main_row" justify="center">
          <v-col :cols="12">
            <div
              id="content-title"
              class="  text-center display-4 text-uppercase pa-10"
              style="color:white"
            >
              I nostri servizi
            </div>
          </v-col>
        </v-row>
      </v-container>
    </section>
    <section class="mx-auto">
      <v-container fill-height>
        <v-row id="main_row" justify="center" align="center">
          <v-col :cols="12">
            <v-card max-width="960px" class="mx-auto pa-5 mt-5" color="blue">
              <v-container fluid>
                <v-row dense>
                  <v-col
                    v-for="service in services"
                    :key="service.title"
                    :cols="service.flex"
                    :md="service.md"
                  >
                    <v-card class="pa-5">
                      <v-img
                        :src="service.src"
                        class="white--text align-end"
                        gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                        height="200px"
                      >
                        <v-card-title
                          class="display-1 font-weight-bold text-uppercase text-center mx-auto"
                          style="margin-left:auto;margin-right:auto"
                          v-text="service.title"
                        ></v-card-title>
                      </v-img>

                      <v-card-actions>
                        <v-spacer></v-spacer>

                        <v-btn outlined color="purple" text :to="service.to">
                          Scopri
                        </v-btn>
                      </v-card-actions>
                    </v-card>
                  </v-col>
                </v-row>
              </v-container>
            </v-card>
          </v-col>
        </v-row>
        <v-row id="main_row" justify="center"> </v-row>
      </v-container>
    </section>
    <FooterLarge class="hidden-sm-and-down" />
  </div>
</template>

<script>
import { FooterLarge } from '@/components/'
export default {
  components: {
    FooterLarge
  },
  layout: 'homepage',
  data() {
    return {
      services: [
        {
          title: 'Percorsi educativi',
          src: require('@/static/percorsi-puppy-school-banner-mobile.jpg'),
          flex: 12,
          md: 4,
          to: '/percorsi/'
        },
        {
          title: 'Bautique',
          src: require('@/static/bautique.jpg'),
          flex: 6,
          md: 4,
          to: './bautique'
        },
        {
          title: 'Wedding dog sitter',
          src: require('@/static/wedding1.jpg'),
          flex: 6,
          md: 4,
          to: './wedding-dog-sitter'
        },
        {
          title: 'Feste di compleanno',
          src: require('@/static/compleanno-home.jpg'),
          flex: 6,
          md: 4,
          to: './compleanno'
        },
        {
          title: 'Osteopatia animale',
          src: require('@/static/osteopatia-home.jpg'),
          flex: 6,
          md: 4,
          to: './osteopatia'
        },
        {
          title: 'Campo di educazione privato',
          src: require('@/static/campo-addestramento-privato.jpg'),
          flex: 12,
          md: 4,
          to: './campo-educazione-privato'
        }
      ]
    }
  }
}
</script>
