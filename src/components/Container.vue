<template>
  <div class="container">
    <slot></slot>
  </div>
</template>

<style scoped lang="scss">
@import "../assets/styles/index.scss";

.container {
  color: $primary-color;
  height: 100%;
  max-width: sizeAuto(1728);
  margin: 0 sizeAuto(96);
}
</style>
