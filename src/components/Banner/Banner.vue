<script setup>
import Container from "../Container.vue";
import SuccessesList from "./SuccessesList.vue";
import Tooths from "./Tooths.vue";
import Intro from "./Intro.vue";
</script>

<template>
  <section class="banner">
    <Container>
      <div class="banner__wrapper">
        <Intro />
        <Tooths />
        <SuccessesList />
      </div>
    </Container>
  </section>
</template>

<style scoped lang="scss">
@import "../../assets/styles/index.scss";

.banner {
  height: sizeAuto(893);
  background: url("../../assets/img/BannerBg.png") no-repeat center;
  background-size: cover;
}

.banner__wrapper {
  display: flex;
  height: 100%;
  align-items: center;
  justify-content: space-between;
}

@media (max-width: 480px) {
  .banner {
    height: sizeAuto(893 * 2);
  }

  .banner__wrapper {
    flex-wrap: wrap;
    align-content: space-evenly;
    justify-content: center;
  }
}
</style>
