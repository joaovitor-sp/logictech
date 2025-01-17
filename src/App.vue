<template>
  <NavBar />
  <router-view />
</template>

<script>
import { RouterLink, RouterView } from "vue-router";
import NavBar from './components/NavBar.vue';

export default {
  components: {
    NavBar
  }
}
</script>