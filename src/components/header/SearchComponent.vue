<template>
  <div class="wrapper">
    <input
      class="search"
      type="text"
      name="search"
      placeholder="Поиск по 100 000 товаров"
    />
  </div>
</template>

<script setup></script>

<style scoped lang="scss">
@import "@/assets/variables";

.wrapper {
  width: 100%;
  position: relative;

  &::before {
    content: "";
    position: absolute;
    width: 24px;
    height: 24px;
    top: 12px;
    left: 16px;
    background: url("@/assets/icons/search.svg") no-repeat center;
  }
}

.search {
  width: 100%;
  border: 1px solid $accent-color;
  border-radius: 10px;
  padding: 12px 16px 12px 48px;
  font-size: 16px;
  line-height: 24px;

  &::placeholder {
    color: #5a5a5a;
  }
}
</style>
