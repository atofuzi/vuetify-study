<template>
  <v-tabs
    class="pt-16"
    v-model="model"
    centered
    slider-color="black"
    color="black"
    background-color="grey lighten-2"
  >
    <v-tab
      v-for="i in tabItems"
      :key="i"
      :href="`#tab-${i}`"
    >
      {{  i }}
    </v-tab>
  </v-tabs>
</template>

<script>
export default {
  data(){
    return {
      tabItems: [
        'すべてのアイテム',
        'シューズアイテム',
        'コスメアイテム'
      ]
    }
  },
}
</script>

<style>

</style>