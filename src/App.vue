<template>
  <v-app>
    <v-app-bar fixed flat max-height="65">
      <Header />
    </v-app-bar>

    <vue-page-transition name="flip-y">
      <router-view></router-view>
    </vue-page-transition>

    <v-footer>
      <Footer />
    </v-footer>
  </v-app>
</template>

<script>
import Header from "./components/common/Header";
import Footer from "./components/common/Footer";

export default {
  name: "App",

  components: {
    Header,
    Footer
  },

  data: () => ({
    //
  })
};
</script>
