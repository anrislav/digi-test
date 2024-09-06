<template>
  <header>
    <div class="desktop">
      <Logo></Logo>
      <Button text="Каталог"></Button>
      <Search></Search>
      <Menu :items="menuItems"></Menu>
    </div>
    <HeaderMobile class="mobile"></HeaderMobile>
  </header>
</template>

<script setup>
import Logo from "./LogoComponent.vue";
import Button from "./ButtonComponent.vue";
import Search from "./SearchComponent.vue";
import Menu from "./MenuComponent.vue";
import HeaderMobile from "./HeaderMobileComponent.vue";

const menuItems = [
  { id: 1, title: "Информация о компании" },
  { id: 2, title: "Контакты" },
  { id: 3, title: "Полезные ссылки" },
];
</script>

<style scoped lang="scss">
.desktop {
  width: 100%;
  display: flex;
  gap: 24px;
  padding: 12px 0;
  margin-bottom: 24px;

  @media screen and (width < 1024px) {
    display: none;
  }
}

.mobile {
  display: none;
  margin-bottom: 12px;

  @media screen and (width < 1024px) {
    display: block;
  }
}
</style>
