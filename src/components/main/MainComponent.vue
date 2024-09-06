<script setup>
import Product from "./ProductComponent.vue";
const products = [
  {
    id: 1,
    title:
      "Полное название товара в несколько строк для вида с обрывом в конце...",
    brand: "Бренд",
    price: 5990,
    fullPrice: 5990,
    discount: 25,
    available: true,
    hit: true,
  },
  {
    id: 2,
    title:
      "Полное название товара в несколько строк для вида с обрывом в конце...",
    brand: "Бренд",
    price: 5990,
    fullPrice: 5990,
    discount: 25,
    available: true,
    hit: true,
  },
  {
    id: 3,
    title:
      "Полное название товара в несколько строк для вида с обрывом в конце...",
    brand: "Бренд",
    discount: 25,
    available: false,
    hit: true,
  },
  {
    id: 4,
    title:
      "Полное название товара в несколько строк для вида с обрывом в конце...",
    brand: "Бренд",
    price: 5990,
    fullPrice: 5990,
    discount: 25,
    available: true,
    hit: true,
  },
  {
    id: 5,
    title:
      "Полное название товара в несколько строк для вида с обрывом в конце...",
    brand: "Бренд",
    price: 5990,
    fullPrice: 5990,
    discount: 25,
    available: true,
    hit: true,
  },
  {
    id: 6,
    title:
      "Полное название товара в несколько строк для вида с обрывом в конце...",
    brand: "Бренд",
    price: 5990,
    fullPrice: 5990,
    discount: 25,
    available: true,
    hit: true,
  },
  {
    id: 7,
    title:
      "Полное название товара в несколько строк для вида с обрывом в конце...",
    brand: "Бренд",
    price: 5990,
    fullPrice: 5990,
    discount: 25,
    available: true,
    hit: true,
  },
  {
    id: 8,
    title:
      "Полное название товара в несколько строк для вида с обрывом в конце...",
    brand: "Бренд",
    price: 5990,
    fullPrice: 5990,
    discount: 25,
    available: true,
    hit: true,
  },
  {
    id: 9,
    title:
      "Полное название товара в несколько строк для вида с обрывом в конце...",
    brand: "Бренд",
    price: 5990,
    fullPrice: 5990,
    discount: 25,
    available: true,
    hit: true,
  },
  {
    id: 10,
    title:
      "Полное название товара в несколько строк для вида с обрывом в конце...",
    brand: "Бренд",
    price: 5990,
    fullPrice: 5990,
    discount: 25,
    available: true,
    hit: true,
  },
  {
    id: 11,
    title:
      "Полное название товара в несколько строк для вида с обрывом в конце...",
    brand: "Бренд",
    price: 5990,
    fullPrice: 5990,
    discount: 25,
    available: true,
    hit: true,
  },
  {
    id: 12,
    title:
      "Полное название товара в несколько строк для вида с обрывом в конце...",
    brand: "Бренд",
    price: 5990,
    fullPrice: 5990,
    discount: 25,
    available: true,
    hit: true,
  },
];
</script>

<template>
  <main class="main">
    <Product
      v-for="product of products"
      :key="product.id"
      :product="product"
    ></Product>
  </main>
</template>

<style scoped lang="scss">
.main {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 24px;
  margin-bottom: 36px;

  @media screen and (width < 1440px) {
    grid-template-columns: repeat(3, 1fr);
  }

  @media screen and (width < 600px) {
    grid-template-columns: repeat(2, 1fr);
    gap: 16px 12px;
  }

  @media screen and (width < 375px) {
    grid-template-columns: 1fr;
  }
}
</style>
