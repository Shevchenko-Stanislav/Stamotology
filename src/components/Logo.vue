<template>
  <a href="#" class="wrapper">
    <img src="../assets/img/Logo.svg" alt="Logo" class="img" />
    <p class="logo__text">32 карата</p>
  </a>
</template>

<style scoped lang="scss">
@import "../assets/styles/index.scss";

.wrapper {
  display: flex;
  align-items: center;
}

.logo__text {
  text-transform: uppercase;
  font-family: "Neue Machina", sans-serif;
  font-weight: 800;
  font-size: sizeAuto(32);
  line-height: 100%;
  color: $theme-color;
  white-space: nowrap;
}

.img {
  width: sizeAuto(32);
  height: sizeAuto(32);
  margin-right: sizeAuto(16);
}
</style>

<script>
export default {
  props: {
    width: {
      type: Number,
    },
    height: {
      type: Number,
    },
  },

  // computed: {
  //   cssVars() {
  //     return {
  //       "--width": this.width + "px",
  //       "--height": this.height + "px",
  //     };
  //   },
  // },
};
</script>
