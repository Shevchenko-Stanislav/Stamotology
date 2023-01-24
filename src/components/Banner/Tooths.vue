<template>
  <div class="wrapper">
    <img
      src="../../assets/img/BigTooth.png"
      alt="MediumTooth"
      class="mediumTooth"
    />
    <img
      src="../../assets/img/BigTooth.png"
      alt="SmallTooth"
      class="smallTooth"
    />
    <img src="../../assets/img/BigTooth.png" alt="BigTooth" class="bigTooth" />
  </div>
</template>

<style scoped lang="scss">
@import "../../assets/styles/index.scss";

.bigTooth {
  max-width: sizeAuto(300);
  height: sizeAuto(420);
}

.mediumTooth {
  max-width: sizeAuto(64);
  height: sizeAuto(90);
  transform: rotate(-35deg);
  align-self: flex-start;
}

.smallTooth {
  max-width: sizeAuto(23);
  height: sizeAuto(33);
  transform: rotate(-20deg);
  align-self: flex-end;
}

.wrapper {
  display: flex;
  margin-right: sizeAuto(50);
}

@media (max-width: 768px) {
  .bigTooth {
    max-width: sizeAuto(250);
    height: sizeAuto(360);
  }
}

@media (max-width: 590px) {
  .wrapper {
    display: none;
  }
}
</style>
