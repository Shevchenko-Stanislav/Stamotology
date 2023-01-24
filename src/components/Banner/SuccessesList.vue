<script setup>
import SuccessesItem from "./SuccessesItem.vue";
</script>

<template>
  <ul class="list">
    <SuccessesItem
      v-for="(item, index) in array"
      :key="index"
      :name="item.name"
      :description="item.description"
    />
  </ul>
</template>

<script>
const data = [
  {
    name: "15 лет",
    description: "Была открыта наша клиника",
  },
  {
    name: "8 дипломов",
    description: "Повышения квалификации полученных в Берлине, Сеуле и Москве",
  },
  {
    name: ">3000 ",
    description: "Человек успешно воспользовались нашими услугами",
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

<style scoped lang="scss">
@import "../../assets/styles/index.scss";

@media (max-width: 480px) {
  .list {
    display: flex;
    flex-wrap: wrap;
  }
}
</style>
