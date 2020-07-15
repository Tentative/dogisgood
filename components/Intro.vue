<template>
  <div>
    <v-sheet id="intro" color="rgba(0,0,0,0)">
      <v-img class="intro_img" :src="banner" />
      <v-sheet class="intro_content" color="#5ea5ef" dark>
        Il nostro cane è un compagno di vita e condivide con noi avventure e
        tempo libero, ma gli impegni quotidiani, spesso, ci tengono fuori casa
        per parecchie ore costringendo il nostro amico a rimanere solo e
        recluso. L’idea del nostro asilo nasce proprio da una riflessione
        intorno alle esigenze di entrambi.
      </v-sheet>
    </v-sheet>
  </div>
</template>

<script>
export default {
  name: 'Intro',
  data() {
    return {
      banner: require('@/static/intro-logo.png')
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/intro.scss';
</style>
