<script setup>
import Container from "../Container.vue";
import ServicesItem from "./ServicesItem.vue";
</script>

<template>
  <Container>
    <section class="wrapper">
      <ul class="list">
        <ServicesItem
          v-for="(item, index) in array"
          v-bind:key="index"
          v-bind:data="item"
        />
      </ul>
    </section>
  </Container>
</template>

<style scoped lang="scss">
@import "../../assets/styles/index.scss";

.wrapper {
  margin-bottom: sizeAuto(192);
}

.list {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: sizeAuto(24);
}
</style>

<script>
const data = [
  {
    name: "Лечение зубов",
    image: "/src/assets/img/TreatmentIcon.svg",
  },
  {
    name: "Протезирование",
    image: "/src/assets/img/ProstheticsIcon.svg",
  },
  {
    name: "Художественная реставрация",
    image: "/src/assets/img/RestorationIcon.svg",
  },
  {
    name: "Имплантация",
    image: "/src/assets/img/ImplantationIcon.svg",
  },
  {
    name: "Хирургия и удаление",
    image: "/src/assets/img/RemovalIcon.svg",
  },
  {
    name: "Отбеливание и чистка",
    image: "/src/assets/img/WhiteningIcon.svg",
  },
];
export default {
  data() {
    return {
      array: data,
    };
  },
};
</script>
