<template>
  <div>
    <div class="item__wrapper" v-if="diraction === `right`">
      <div class="section text_block right_arrow">
        <h3 class="title">{{ title }}</h3>
        <p class="description">
          {{ description }}
        </p>
      </div>
      <div class="section">
        <img :src="img" />
      </div>
    </div>

    <div class="item__wrapper" v-if="diraction === `left`">
      <div class="section">
        <img :src="img" />
      </div>
      <div class="section text_block left_arrow">
        <h3 class="title">{{ title }}</h3>
        <p class="description">
          {{ description }}
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
@import "/src/assets/styles/index.scss";

.item__wrapper {
  display: flex;
}

.section {
  width: stretchSize(414);
  height: stretchSize(438);

  img {
    object-fit: fill;
    width: 100%;
    height: 100%;
  }
}

.text_block {
  display: flex;
  flex-wrap: wrap;
  align-content: space-between;
  position: relative;
  padding: sizeAuto(12);

  .title {
    font-weight: 600;
    font-size: sizeAuto(32);
    color: $primary-color;
  }

  .description {
    font-weight: 400;
    font-size: sizeAuto(24);
    color: $secondary-color;
  }
}

.right_arrow:after {
  position: absolute;
  left: 99%;
  top: 0;
  border: sizeAuto(50) solid transparent;
  border-left: sizeAuto(80) solid white;
  height: 20%;
  content: "";
}

.left_arrow::after {
  position: absolute;
  right: 99%;
  top: 0;
  border: sizeAuto(50) solid transparent;
  border-right: sizeAuto(80) solid white;
  height: 20%;
  content: "";
}

@media (max-width: 680px) {
  .section {
    width: 100%;
    height: 100%;
  }
  .text_block {
    padding: 0 sizeAuto(8);

    .title {
      font-size: sizeAuto(28);
    }

    .description {
      font-size: sizeAuto(20);
    }
  }
}
</style>

<script>
export default {
  data() {
    return { diraction: this.imageDiraction };
  },
  props: {
    imageDiraction: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    img: {
      type: String,
      required: true,
    },
  },
};
</script>
