<script setup>
import Header from "./components/Header.vue";
import Footer from "./components/Footer/Footer.vue";
import HomePage from "./pages/HomePage.vue";
</script>

<template>
  <div id="app">
    <div class="page">
      <Header />
      <main><HomePage /></main>
      <Footer />
    </div>
  </div>
</template>

<style lang="scss">
@import "./assets/styles/index.scss";
</style>
