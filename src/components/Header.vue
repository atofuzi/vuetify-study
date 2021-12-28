<template>
  <div>
        <v-app-bar
          style="margin: 0 auto;"
          fixed
          color="grey lighten-2"
          elevate-on-scroll
          height="64px"
        >
          <v-sheet 
            width="80%"
            class="d-flex align-center"
            color="grey lighten-2"
            style="margin: 0 auto">
            <v-toolbar-title class="font-weight-black">GOTOTOWN</v-toolbar-title>
            <v-text-field
              class="pl-6"
              rounded
              label="すべてのアイテムから探す"
              prepend-inner-icon="mdi-magnify"
              background-color="white"
              hide-details
            ></v-text-field>
            <v-spacer></v-spacer>
            <v-btn depressed color="grey lighten-2">
              ログイン
            </v-btn>

            <v-btn icon>
              <v-icon>mdi-magnify</v-icon>
            </v-btn>

            <v-btn icon>
              <v-icon>mdi-heart</v-icon>
            </v-btn>

            <v-btn icon>
              <v-icon>mdi-dots-vertical</v-icon>
            </v-btn>
          </v-sheet>
        </v-app-bar>
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
  </div>
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
  }

}
</script>

<style>

</style>