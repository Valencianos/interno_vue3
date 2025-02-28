<script setup lang="ts">

defineProps({
  pageNumber: {
    type: Number,
    default: 1
  }
})
</script>

<template>
  <button class="page-button" type="button">
    <span class="page-number" v-if="pageNumber < 10">0{{ pageNumber }}</span>
    <span class="page-number" v-else>{{ pageNumber }}</span>
  </button>
</template>

<style scoped lang="scss">
@use '@/assets/styles/_vars.scss' as *;
.page-button {
  border-radius: 50%;
  border: 1px solid $primary;
  background-color: transparent;
  width: 52px;
  height: 52px;
  flex-shrink: 0;
  text-align: center;
}
.page-number {
  color: $secondary;
  font-family: $primary-font;
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: 150%;
  text-transform: capitalize;
}
</style>