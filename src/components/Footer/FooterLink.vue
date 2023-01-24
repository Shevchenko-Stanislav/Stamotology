<template>
  <div class="wrapper">
    <img src="/src/assets/img/LinkIcon.svg" alt="link-icon" />
    <a href="#!">{{ linkTitle }}</a>
  </div>
</template>

<style scoped lang="scss">
@import "/src/assets/styles/index.scss";

.wrapper {
  min-width: 100%;
  display: flex;
  border: 2px solid $secondary-color;
  padding: sizeAuto(16);
  color: $theme-color;
  align-items: center;

  a {
    font-family: "Neue Machina", sans-serif;
    font-weight: 400;
    font-size: sizeAuto(40);
  }

  img {
    margin-right: sizeAuto(50);
    width: sizeAuto(48);
    height: sizeAuto(48);
  }
}

@media (max-width: 590px) {
  .wrapper:not(:last-child) {
    margin-bottom: sizeAuto(32);
  }
}
</style>

<script>
export default {
  props: {
    linkTitle: {
      type: String,
      required: true,
    },
  },
};
</script>
