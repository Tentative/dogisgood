<template>
  <div>
    <section id="bautique">
      <v-carousel>
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
            Gallery
          </div>
        </v-carousel-item>
      </v-carousel>
    </section>
    <v-row justify="center" class="hidden-sm-and-down">
      <v-img :src="src" max-width="200px" height="200px" />
    </v-row>

    <FooterLarge
      style="position:absolute;bottom:0;width:100%"
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
      src: require('@/static/logo-circle.png'),
      items: [
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg'
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg'
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg'
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg'
        }
      ]
    }
  }
}
</script>
