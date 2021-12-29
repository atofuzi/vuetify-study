<template>
  <div>
        <v-app-bar
          class="mx-auto"
          fixed
          color="grey lighten-2"
          elevate-on-scroll
          height="64px"
        >
          <v-sheet 
            width="80%"
            class="d-flex align-center mx-auto"
            color="grey lighten-2"
            >
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
      <HeaderTab></HeaderTab>
      <HeaderNavigation></HeaderNavigation> 
  </div>
</template>

<script>
import HeaderNavigation from "./HeaderNavigation.vue"
import HeaderTab from "./HeaderTab.vue"
export default {
  components: {
    HeaderNavigation,
    HeaderTab
  }

}
</script>

<style>

</style>