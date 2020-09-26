<template>
  <div id="app">
    <Navbar appTitle="Flip Image" />
    <MainContent />
    <Footer />
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Navbar from "./components/navbar.vue";
import Footer from "./components/footer.vue";
import MainContent from "./components/main-content.vue";

export default Vue.extend({
  name: "App",
  components: {
    Navbar,
    MainContent,
    Footer
  }
});
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
</style>
