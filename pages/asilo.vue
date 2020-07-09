<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 class="main-banner">
      <Logo :img-src="imgSrc" />
    </v-flex>
  </v-layout>
</template>

<script>
import Logo from '@/components/Logo.vue'
export default {
  components: {
    Logo
  },
  data() {
    return {
      imgSrc: 'asilo'
    }
  },
  layout: 'homepage'
}
</script>
