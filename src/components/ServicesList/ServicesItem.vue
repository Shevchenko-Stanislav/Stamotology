<template>
  <li class="item">
    <img :src="data.image" :alt="data.name" class="img" />
    <a class="item__name" href="#">{{ data.name }}</a>
    <div class="description">
      <p class="description__text">Подробнее об услуге</p>
      <a>
        <img src="/src/assets/img/RedirectIcon.svg" class="redirect-icon" />
      </a>
    </div>
  </li>
</template>

<style scoped lang="scss">
@import "../../assets/styles/index.scss";

.item {
  display: flex;
  flex-direction: column;
  padding: sizeAuto(40);
  box-shadow: 0px 4px 32px 0px #f1f1fa;
  width: sizeAuto(560);

  &__name {
    margin-bottom: sizeAuto(24);
    font-family: "Manpore", sans-serif;
    font-size: sizeAuto(32);
    line-height: sizeAuto(44);
    font-weight: 600;
    color: $primary-color;
  }

  &:hover {
    scale: 1.05;
  }
}

.description {
  display: flex;
  justify-content: space-between;

  &__text {
    font-family: "Manpore", sans-serif;
    font-size: sizeAuto(24);
    line-height: sizeAuto(32);
    font-weight: 400;
    color: $secondary-color;
  }
}

.img {
  width: sizeAuto(140);
  height: sizeAuto(115);
  margin-bottom: sizeAuto(40);
}
</style>

<script>
export default {
  props: {
    data: {
      require: true,
      type: Object,
      default() {
        return {};
      },
    },
  },
};
</script>
