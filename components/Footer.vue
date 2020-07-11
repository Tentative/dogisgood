<template>
  <v-footer light padless>
    <v-card
      flat
      tile
      width="100vw"
      color="#42a5f5"
      dark
      shaped
      class=" text-center"
    >
      <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4"
          icon
          :href="icon.to"
        >
          <v-icon size="24px">{{ icon.icon }}</v-icon>
        </v-btn>
        <v-btn
          class="mx-4"
          icon
          href="https://www.tiktok.com/@asilodogisgood"
          target="blank"
        >
          <div class="tiktok"><tiktok /></div
        ></v-btn>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
import tiktok from '@/components/tiktok.vue'
export default {
  name: 'Footer',
  components: {
    tiktok
  },
  data() {
    return {
      icons: [
        {
          icon: 'mdi-whatsapp',
          to: 'https://wa.me/393397268386'
        },
        {
          icon: 'mdi-facebook',
          to: 'https://www.facebook.com/asilodogisgood/'
        },
        {
          icon: 'mdi-instagram',
          to: 'https://www.instagram.com/asilodogisgood/'
        }
      ]
    }
  }
}
</script>
