<template>
  <div>
    <section id="bautique" style="height:100vh">
      <v-carousel height="100vh">
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
          title: 'Campo di addestramento privato'
        },
        {
          src: require('@/static/gallery/camp3.JPG'),
          title: 'Campo di addestramento privato'
        },
        {
          src: require('@/static/gallery/compleanni-1.jpg'),
          title: 'Feste di compleanno'
        },
        {
          src: require('@/static/gallery/compleanni-2.JPG'),
          title: 'Feste di compleanno'
        },
        {
          src: require('@/static/gallery/compleanni-3.JPG'),
          title: 'Feste di compleanno'
        },
        {
          src: require('@/static/gallery/compleanni-4.JPG'),
          title: 'Feste di compleanno'
        },
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
      ]
    }
  }
}
</script>
