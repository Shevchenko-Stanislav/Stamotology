<script setup>
import Container from "../Container.vue";
import FooterLink from "./FooterLink.vue";
import Logo from "../Logo.vue";
</script>

<template>
  <footer>
    <Container>
      <div class="footer__wrapper">
        <div class="info">
          <Logo />
          <a href="tel:+79036995150" class="tel"><p>+7 903 699-51-50</p></a>
          <p class="timetable">
            пн-пт с 9:00-19:00, сб с 10:00 до 15:00 (по предварительной записи)
          </p>
        </div>
        <div class="links">
          <FooterLink linkTitle="Наша лицензия" />
          <FooterLink linkTitle="Гарантии" />
        </div>
      </div>
    </Container>
  </footer>
</template>

<style scoped lang="scss">
@import "/src/assets/styles/index.scss";

footer {
  background-color: #250450;
}

.footer__wrapper {
  display: flex;
  padding: sizeAuto(50) 0;

  .info {
    min-width: 50%;
  }

  .tel {
    display: block;
    font-weight: 400;
    font-size: sizeAuto(40);
    margin-top: sizeAuto(48);
    margin-bottom: sizeAuto(16);
  }

  .timetable {
    color: $secondary-color;
    font-weight: 300;
    font-size: sizeAuto(32);
    max-width: 65%;
  }

  .links {
    min-width: 50%;
    display: flex;
    flex-wrap: wrap;
    align-content: space-between;
  }

  p {
    color: $theme-color;
    font-family: "Neune Machina", sans-serif;
  }
}

@media (max-width: 590px) {
  .footer__wrapper {
    display: block;

    .info {
      min-width: 100%;
      margin-bottom: sizeAuto(32);
    }

    .links {
      min-width: 100%;
    }
  }
}
</style>
