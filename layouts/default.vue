<template>
  <v-app>
    <nav-bar />
    <Banner />
    <About />
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <Footer />
  </v-app>
</template>

<script>
import navBar from "../components/navBar.vue";
import footer from "../components/footer.vue";
import Banner from '../components/Banner.vue';
import About from '../components/About-us.vue'
export default {
  components: {
    navBar,
    footer,
    Banner,
    About
  },
  data() {
    return {};
  },
  created() {
    this.$vuetify.rtl = true;
  },
};
</script>
