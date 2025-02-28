<script setup lang="ts">

import LinkButton from "@/components/ui/buttons/LinkButton.vue";
</script>

<template>
  <section class="hero">
    <div class="container">
      <div class="hero__wrapper">
        <div class="hero__box">
          <h1 class="hero__title">Let Your Home Be Unique</h1>
          <p class="hero__text">There are many variations of the passages of lorem Ipsum fromavailable, majority.</p>
          <link-button button-title="Get Started" />
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped lang="scss">
@use '@/assets/styles/_vars.scss' as *;
.hero {
  max-height: 758px;
  margin-bottom: 96px;
  &__wrapper {
    background-image: url('@/assets/img/banners/main_banner.png');
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    border-radius: 70px;
    fill: $secondary;
  }
  &__box {
    padding-top: 208px;
    padding-bottom: 208px;
    padding-left: 52px;
  }
  &__title {
    font-family: $secondary-font;
    font-size: 65px;
    font-weight: 400;
    color: $secondary;
    -webkit-text-stroke-width: 1px;
    -webkit-text-stroke-color: #000;
    margin-bottom: 18px;
    max-width: 500px;
    line-height: 1.25;
  }
  &__text {
    font-family: $primary-font;
    font-size: 22px;
    line-height: 1.5;
    font-weight: 400;
    letter-spacing: 0.01em;
    color: #4D5053;
    max-width: 432px;
    margin-bottom: 21px;
  }
}
</style>