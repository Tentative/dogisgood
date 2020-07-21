<template>
  <div>
    <v-img id="footer_logo" :src="src" />
    <v-row id="container_row">
      <v-col class="container_col_sx" :cols="6">
        <v-row class="empty_row"> </v-row>
        <v-row class="short_row">
          <v-sheet color="red">asdadasda</v-sheet>
        </v-row>
      </v-col>
      <v-col class="container_col_dx" :cols="6">
        <v-row class="high_row">asdasd</v-row>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: 'End',
  data() {
    return {
      src: require('@/static/logo-circle.png')
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/end.scss';
</style>
