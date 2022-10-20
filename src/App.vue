<script setup>
import Navigator from "./components/Navigator.vue";
import Carusel from "./components/Carusel.vue";
import Specials from "./components/specials/Specials.vue";
import Menus from "./components/menus/Menus.vue";
import Chefs from "./components/chefs/Chefs.vue";
import Footer from "./components/Footer.vue";

const views = [Carusel, Specials, Menus, Chefs];
</script>

<template>
  <!-- Navbar -->
  <Navigator />
  <!-- Components views -->
  <component
    ref="view"
    :is="view"
    v-for="(view, index) in views"
    :key="index"
  />
  <!-- Footer -->
  <Footer />
</template>

<style scoped>
</style>
