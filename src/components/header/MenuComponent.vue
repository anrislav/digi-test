<template>
  <ul class="menu">
    <li :key="item.id" v-for="item of items">
      <a class="item" href="#">{{ item.title }}</a>
    </li>
  </ul>
</template>

<script setup>
defineProps(["items"]);
</script>

<style scoped lang="scss">
@import "@/assets/variables";

.menu {
  margin: 0;
  padding: 0;
  list-style-type: none;
  display: flex;
  flex-shrink: 0;
  gap: 20px;
  align-items: center;
}

.item {
  text-decoration: none;
  color: #393939;
  padding: 13px 0;

  &:hover {
    color: $accent-color;
    border-bottom: 1px solid $accent-color;
  }
}
</style>
