<template>

  <v-card
    class="d-flex mt-6 mx-auto"
    flat
    tile
    width="80%"
  >
    <v-btn
      depressed
      class="pa-2 font-weight-bold"
    >
      すべて
    </v-btn>
    <v-btn
      class="pa-2 font-weight-bold"
      color="blue darken-4"
      plain
    >
      <v-icon small>mdi-human-male</v-icon>メンズ
    </v-btn>
    <v-btn
      class="pa-2 font-weight-bold"
      color="red darken-3"
      plain
      text
    >
      <v-icon small>mdi-human-female</v-icon>レディース
    </v-btn>
    <v-btn
      class="pa-2 font-weight-bold"
      color="amber accent-3"
      plain
    >
      <v-icon x-small>mdi-human-male</v-icon>キッズ
    </v-btn>
    <v-btn
      class="pa-2 ml-auto"
      plain
    >
      GOTOTOWNからのお知らせ
    </v-btn>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
    }
  }
}
</script>

<style>

</style>