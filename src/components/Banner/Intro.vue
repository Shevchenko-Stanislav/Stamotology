<template>
  <div class="intro">
    <h1 class="intro__header">Засияй по новому</h1>
    <button class="btn" v-on:click="subscribeOnConsultation">
      Записаться на консультацию
    </button>
  </div>
</template>

<script>
export default {
  methods: {
    subscribeOnConsultation() {
      alert("In Dev");
    },
  },
};
</script>

<style scoped lang="scss">
@import "../../assets/styles/index.scss";

.intro {
  max-width: sizeAuto(583);
  margin-right: sizeAuto(12);

  &__header {
    font-family: "Neue Machina", sans-serif;
    font-weight: 800;
    font-size: sizeAuto(104);
    line-height: 100%;
    color: $theme-color;
    margin-bottom: sizeAuto(68);
  }
}

.btn {
  font-family: "Manrope", sans-serif;
  font-weight: 700;
  font-size: sizeAuto(16);
  color: $secondary-color;
  padding: sizeAuto(24);
  border: none;
  border-radius: sizeAuto(12);
}

.btn:hover {
  opacity: 0.8;
  cursor: pointer;
}

@media (max-width: 850px) {
  .intro__header {
    font-size: sizeAuto(78);
  }
}

@media (max-width: 768px) {
  .intro__header {
    font-size: sizeAuto(72);
  }
}

@media (max-width: 480px) {
  .intro {
    display: flex;
    justify-content: center;
    flex-direction: column;
    margin-right: 0;
  }

  .intro__header {
    text-align: center;
    font-size: sizeAuto(92);
  }

  .btn {
    font-size: sizeAuto(36);
  }
}
</style>
