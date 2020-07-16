<template>
  <div>
    <v-simple-table>
      <template v-slot:default>
        <thead>
          <tr id="shape">
            <th class="text-left shape-left">&nbsp;</th>
            <th class="text-right shape-right">Servizi</th>
          </tr>
        </thead>
      </template>
    </v-simple-table>

    <v-row id="shape-content">
      <v-col class="col-md-4 shape-content-left">asdasd</v-col>
      <v-col class="col-md-8 shape-content-right">asdasda</v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: 'Service'
}
</script>

<style lang="scss" scoped>
@import '@/assets/service.scss';
</style>
