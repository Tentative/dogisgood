<template>
  <div>
    <section id="bautique" class="hidden-sm-and-down">
      <v-carousel cycle height="100vh" interval="3000" hide-delimiters>
        <v-carousel-item
          v-for="(item, i) in items"
          :key="i"
          :src="item.src"
          reverse-transition="fade-transition"
          transition="fade-transition"
          ><div
            style="background-color:rgba(0,0,0,0.54)"
            class="subheading pa-5 text-center white--text text-uppercase "
          >
            {{ item.title }}
          </div>
        </v-carousel-item>
      </v-carousel>
    </section>
    <section id="bautique" class="hidden-md-and-up">
      <v-carousel cycle interval="3000" hide-delimiters>
        <v-carousel-item
          v-for="(item, i) in mobile"
          :key="i"
          :src="item.src"
          reverse-transition="fade-transition"
          transition="fade-transition"
          cover
          style="margin-top:0"
          ><div
            style="background-color:rgba(0,0,0,0.54)"
            class="subheading pa-5 text-center white--text text-uppercase "
          >
            {{ item.title }}
          </div>
        </v-carousel-item>
      </v-carousel>
      <div class="display-1 primary--text text-center mt-5">
        Asilo per cani Dog Is Good
      </div>
      <div class="headline text-center primary--text mt-2">
        Via San Vitale 129 - Seregno (MB)
      </div>
      <v-row class="mt-5 mx-auto" justify="center">
        <v-img :src="logo" height="250" width="auto" contain="" />
      </v-row>
    </section>

    <FooterLarge
      style="position:relative;bottom:0;width:100%"
      class="hidden-sm-and-down"
    />
  </div>
</template>

<script>
import { FooterLarge } from '@/components'

export default {
  name: 'Gallery',
  layout: 'homepage',

  components: {
    FooterLarge
  },
  data() {
    return {
      logo: require('@/static/logo.jpg'),
      items: [
        {
          src: require('@/static/gallery/bautique-4.jpg'),
          title: 'Bautique'
        },
        {
          src: require('@/static/gallery/bautique-5.jpg'),
          title: 'Bautique'
        },
        {
          src: require('@/static/gallery/camp.JPG'),
          title: 'Campo di educazione privato'
        },
        {
          src: require('@/static/gallery/camp3.JPG'),
          title: 'Campo di educazione privato'
        },
        {
          src: require('@/static/gallery/compleanni-1.jpg'),
          title: 'Feste di compleanno'
        },
        {
          src: require('@/static/compleanno-5.JPG'),
          title: 'Feste di compleanno'
        },
        // {
        //   src: require('@/static/gallery/compleanni-1.jpg'),
        //   title: 'Feste di compleanno'
        // },
        // {
        //   src: require('@/static/gallery/compleanni-2.JPG'),
        //   title: 'Feste di compleanno'
        // },
        // {
        //   src: require('@/static/gallery/compleanni-3.JPG'),
        //   title: 'Feste di compleanno'
        // },
        // {
        //   src: require('@/static/gallery/compleanni-4.JPG'),
        //   title: 'Feste di compleanno'
        // },
        {
          src: require('@/static/gallery/compleanni-5.JPG'),
          title: 'Feste di compleanno'
        },
        {
          src: require('@/static/gallery/asilo-1.jpg'),
          title: "L'asilo"
        },
        {
          src: require('@/static/gallery/asilo-2.jpg'),
          title: "Attività all'aperto"
        },
        {
          src: require('@/static/gallery/asilo-3.jpg'),
          title: "L'asilo"
        },
        {
          src: require('@/static/gallery/asilo-4.jpg'),
          title: "L'asilo"
        },
        {
          src: require('@/static/gallery/asilo-5.jpg'),
          title: "L'asilo"
        },
        {
          src: require('@/static/gallery/asilo-6.jpg'),
          title: "L'asilo"
        },
        {
          src: require('@/static/gallery/asilo-7.jpg'),
          title: "L'asilo"
        },
        {
          src: require('@/static/gallery/struttura-1.jpg'),
          title: 'Palestra'
        },
        {
          src: require('@/static/gallery/toelettatura.jpg'),
          title: 'Toelettatura'
        }
      ],
      mobile: [
        {
          src: require('@/static/gallery/bautique-4.jpg'),
          title: 'Bautique'
        },
        {
          src: require('@/static/gallery/bautique-5.jpg'),
          title: 'Bautique'
        },
        {
          src: require('@/static/gallery/camp.JPG'),
          title: 'Campo di educazione privato'
        },
        {
          src: require('@/static/gallery/camp3.JPG'),
          title: 'Campo di educazione privato'
        },
        // {
        //   src: require('@/static/gallery/compleanni-1.jpg'),
        //   title: 'Feste di compleanno'
        // },
        // {
        //   src: require('@/static/gallery/compleanni-2.JPG'),
        //   title: 'Feste di compleanno'
        // },
        // {
        //   src: require('@/static/gallery/compleanni-3.JPG'),
        //   title: 'Feste di compleanno'
        // },
        // {
        //   src: require('@/static/gallery/compleanni-4.JPG'),
        //   title: 'Feste di compleanno'
        // },
        // {
        //   src: require('@/static/gallery/compleanni-5.JPG'),
        //   title: 'Feste di compleanno'
        // },
        {
          src: require('@/static/gallery/asilo-1.jpg'),
          title: "L'asilo"
        },
        {
          src: require('@/static/gallery/asilo-2.jpg'),
          title: "Attività all'aperto"
        },
        {
          src: require('@/static/gallery/asilo-3.jpg'),
          title: "L'asilo"
        },
        {
          src: require('@/static/gallery/asilo-4.jpg'),
          title: "L'asilo"
        },
        {
          src: require('@/static/gallery/asilo-5.jpg'),
          title: "L'asilo"
        },
        {
          src: require('@/static/gallery/asilo-6.jpg'),
          title: "L'asilo"
        },
        {
          src: require('@/static/gallery/asilo-7.jpg'),
          title: "L'asilo"
        },
        {
          src: require('@/static/gallery/struttura-1.jpg'),
          title: 'Palestra'
        },
        {
          src: require('@/static/gallery/toelettatura.jpg'),
          title: 'Toelettatura'
        }
      ]
    }
  }
}
</script>
