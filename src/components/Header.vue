<script setup>
import Logo from "./Logo.vue";
import Container from "./Container.vue";
</script>

<template>
  <header class="header">
    <Container>
      <div class="wrapper">
        <Logo />
        <nav class="navigation">
          <ul class="navigation__list">
            <li class="navigation__item">
              <a href="#">Услуги</a>
            </li>
            <li class="navigation__item">
              <a href="#">Клиника</a>
            </li>
            <li class="navigation__item">
              <a href="#">Контакты</a>
            </li>
          </ul>
        </nav>
      </div>
    </Container>
  </header>
</template>

<style scoped lang="scss">
@import "../assets/styles/index.scss";

.header {
  position: absolute;
  width: 100%;
  padding: sizeAuto(34) 0;
  background-color: #ffffff1a;
  top: 0;
  left: 0;
}

.navigation {
  display: flex;
  width: 100%;
  justify-content: center;
}

.navigation__list {
  width: sizeAuto(500);
  line-height: sizeAuto(32);
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.navigation__item {
  color: $theme-color;
  font-size: sizeAuto(16);
  font-weight: 900;
}

.wrapper {
  display: flex;
}

@media (max-width: 1024px) {
  .navigation__item {
    font-size: sizeAuto(24);
  }
}

@media (max-width: 768px) {
  .navigation__item {
    font-size: sizeAuto(26);
  }
}

@media (max-width: 480px) {
  .navigation {
    display: none;
  }
}
</style>
