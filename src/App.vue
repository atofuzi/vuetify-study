<template>
  <v-app>
    <Header></Header>
    <v-main> 
      <div id="home-body">
        <v-container class="home-body-container">
          <v-row no-gutters>
            <v-col
            class="col-6 col-md-2"
            >
              <SideBar></SideBar>
            </v-col>
            <v-col
              class="col-12 col-sm-6 col-md-10"
            >
              <router-view/>
            </v-col>
          </v-row>
       

        </v-container>
      </div>
    </v-main>
  </v-app>
</template>

<script>
import Header from "./components/Header.vue"
import SideBar from "./components/SideBar.vue"

export default {
  name: 'App',

  data: () => ({
    //
  }),
  components: {
    Header,
    SideBar
}
};
</script>
