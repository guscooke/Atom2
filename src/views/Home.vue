<template>
  <v-content>
    <Hero />
    <WeDo />
    <Gallery />
    <Service />
  </v-content>
</template>

<script>
import Hero from "../components/Hero";
import Gallery from "../components/Gallery";
import WeDo from "../components/WeDo";
import Service from "../components/Service";
//import Features from "../components/Features";

export default {
  name: "Home",

  components: {
    Hero,
    Gallery,
    WeDo,
    Service
    //Features
  }
};
</script>
