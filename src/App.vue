<template>
  <NavBar />
  <router-view />
  <Footer />
</template>

<script>
import { RouterLink, RouterView } from "vue-router";
import NavBar from './components/NavBar.vue';
import  Footer from './components/Footer.vue';

export default {
  components: {
    NavBar,
    Footer
  }
}
</script>