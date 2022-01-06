<template>
  <v-app>
    <toolbar />
    <v-content style="background-color: white">
      <!-- <HelloWorld /> -->
      <router-view />
    </v-content>
    <!-- <footer /> -->
  </v-app>

      
</template>

<script>
import Toolbar from "./components/Toolbar.vue";
// import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    // HelloWorld,
    Toolbar,
    // Footer

  },
  data: () => ({
    //
  })
};
</script>
