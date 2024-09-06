<template>
  <button>
    {{ text }}
  </button>
</template>

<script setup>
defineProps(["text"]);
</script>

<style scoped lang="scss">
@import "@/assets/variables";

button {
  cursor: pointer;
  background-color: #fff;
  border: 1px solid $accent-color;
  border-radius: 8px;
  padding: 8px 24px;
  font-size: inherit;
  line-height: 16.94px;
  font-weight: 500;
  transition: all 0.2s ease-in-out;

  &:hover {
    background-color: $accent-color;
    color: #fff;
  }
}
</style>
