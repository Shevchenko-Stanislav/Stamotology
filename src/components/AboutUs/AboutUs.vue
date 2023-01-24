<script setup>
import Container from "../Container.vue";
import AboutUsItem from "./AboutUsItem.vue";
</script>

<template>
  <Container>
    <section>
      <div class="wrapper">
        <AboutUsItem
          :imageDiraction="'right'"
          :title="'Мы принимаем к оплате банковские карты'"
          :description="'Для нас важен комфорт клиента, поэтому мы приобрели терминал'"
          :img="'/src/assets/img/PaymentImage.png'"
        />
        <AboutUsItem
          :imageDiraction="'right'"
          :title="'Мы принимаем к оплате банковские карты'"
          :description="'Для нас важен комфорт клиента, поэтому мы приобрели терминал'"
          :img="'/src/assets/img/Professionals.png'"
        />
        <AboutUsItem
          :imageDiraction="'left'"
          :title="'Мы принимаем к оплате банковские карты'"
          :description="'Для нас важен комфорт клиента, поэтому мы приобрели терминал'"
          :img="'/src/assets/img/Equipment.png'"
        />
        <AboutUsItem
          :imageDiraction="'left'"
          :title="'Мы принимаем к оплате банковские карты'"
          :description="'Для нас важен комфорт клиента, поэтому мы приобрели терминал'"
          :img="'/src/assets/img/ComfortForPatients.png'"
        />
      </div>
    </section>
  </Container>
</template>

<style scoped lang="scss">
@import "/src/assets/styles/index.scss";

.wrapper {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
</style>
