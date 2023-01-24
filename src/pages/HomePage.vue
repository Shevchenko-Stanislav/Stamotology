<script setup>
import Banner from "../components/Banner/Banner.vue";
import ServicesList from "../components/ServicesList/ServicesList.vue";
import AboutUs from "../components/AboutUs/AboutUs.vue";
</script>

<template>
  <div class="wrapper">
    <Banner />
    <section class="content">
      <ServicesList />
      <AboutUs />
    </section>
  </div>
</template>

<style scoped lang="scss">
@import "../assets/styles/index.scss";

.content {
  padding: sizeAuto(128) 0;
  background-color: $theme-color;
}
</style>
