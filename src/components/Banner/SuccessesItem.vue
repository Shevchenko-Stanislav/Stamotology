<template>
  <li class="item">
    <h2 class="header">
      {{ name }}
    </h2>
    <p class="description">
      {{ description }}
    </p>
  </li>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped lang="scss">
@import "../../assets/styles/index.scss";

.item {
  background: linear-gradient(
    to right,
    rgba(255, 255, 255, 0.2),
    rgba(255, 255, 255, 0)
  );
  width: sizeAuto(414);
  padding: sizeAuto(32);

  &:not(:last-child) {
    margin-bottom: sizeAuto(32);
  }
}

.header {
  font-family: "Neue Machina", sans-serif;
  font-weight: 800;
  font-size: sizeAuto(40);
  line-height: 100%;
  color: $theme-color;
  margin-bottom: sizeAuto(10);
}

.description {
  font-family: "Manrope", sans-serif;
  font-weight: 500;
  font-size: sizeAuto(16);
  line-height: 100%;
  color: $theme-color;
}

@media (max-width: 768px) {
  .item {
    width: sizeAuto(364);
    padding: sizeAuto(24);

    &:not(:last-child) {
      margin-bottom: sizeAuto(32);
    }
  }
}

@media (max-width: 480px) {
  .header {
    font-size: sizeAuto(48);
  }

  .description {
    font-size: sizeAuto(32);
  }

  .item {
    width: 100%;
    padding: sizeAuto(48);

    &:not(:last-child) {
      margin-bottom: sizeAuto(48);
    }
  }
}
</style>
