<script setup lang="ts">
defineProps({
  buttonTitle: {
    type: String,
    required: true,
  }
})
</script>

<template>
  <button class="button">{{ buttonTitle }}</button>
</template>

<style scoped lang="scss">
@use "@/assets/styles/vars.scss" as *;
.button {
  border-radius: 18px;
  padding: 26px 54px;
  box-shadow: 0 10px 20px 0 rgba(192, 192, 192, 0.35);
  background: $secondary;
  font-family: $primary-font;
  font-weight: 600;
  font-size: $font-size-xxs;
  line-height: 1.25;
  letter-spacing: 0.02em;
  color: #fff;
  display: flex;
  gap: 10px;
  align-items: center;
  transition-duration: 0.2s;
  transition-timing-function: ease;

  &:hover {
    background-color: $primary;
    &::after {
      background-image: url('@/assets/img/icons/sec_arrow.svg')
    }
  }

  &:active {
    transform: scale(0.9)
  }

  &::after {
    content: '';
    display: block;
    background-image: url('@/assets/img/icons/primary_arrow.svg');
    width: 18px;
    height: 17px;
  }
}
</style>