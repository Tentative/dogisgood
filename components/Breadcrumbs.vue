<template>
  <v-breadcrumbs :items="items" divider=">"></v-breadcrumbs>
</template>

<script>
export default {
  name: 'Breadcrumbs',
  props: {
    levels: {
      type: Number,
      required: true
    }
  },
  data() {
    return {
      items: []
    }
  },
  created() {
    this.get_path()
    console.log(this.$router.options.routes)
  },
  methods: {
    get_path() {
      for (let level = 0; level <= this.levels; level++) {
        this.items.push({
          text: level === 0 ? 'Homepage' : this.$route.name,
          to: this.$router.options.routes[level].path
        })
      }
    }
  }
}
</script>
