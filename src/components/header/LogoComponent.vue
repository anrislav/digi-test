<template>
  <a href="#" class="logo">
    <Logo class="icon"></Logo>
    <span>Логотип</span>
  </a>
</template>

<script setup>
import Logo from "@/components/icons/LogoIcon.vue";
</script>

<style scoped lang="scss">
@import "@/assets/variables";

.logo {
  display: flex;
  align-items: center;
  gap: 8px;
  height: 48px;
  padding: 0 24px;
  line-height: 20px;
  font-size: 16px;
  color: #000;
  text-decoration: none;

  .icon {
    padding: 3px;
    width: 24px;
    height: 24px;
    color: $accent-color;
  }
}
</style>
