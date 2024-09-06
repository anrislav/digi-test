<script setup>
defineProps(["product"]);
</script>

<template>
  <div class="product">
    <a href="#" class="image">
      <img src="@/assets/product-default.png" alt="" />
      <span class="hit">Хит продаж</span>
      <span class="discount">{{ product.discount }}%</span>
    </a>
    <div class="title-wrapper">
      <a href="#" class="brand">{{ product.brand }}</a>
      <a href="#" class="title">{{ product.title }}</a>
    </div>
    <div class="price-wrapper" v-if="product.available">
      <span class="price">{{ product.price }} ₽</span>
      <span class="full-price">{{ product.fullPrice }} ₽</span>
    </div>
    <a class="button" href="#" v-if="product.available">Купить</a>
    <a class="button button--disabled" href="#" v-else
      >Сообщить о поступлении</a
    >
  </div>
</template>

<style scoped lang="scss">
@import "@/assets/variables";

a {
  color: inherit;
  text-decoration: none;
}

.product {
  display: flex;
  flex-direction: column;
  gap: 16px;
}

.image {
  position: relative;
  height: 200px;
  overflow: hidden;

  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
    transition: scale 0.2s ease-in-out;
  }

  &:hover img {
    scale: 1.3;
  }

  .hit {
    position: absolute;
    top: 12px;
    left: 12px;
    background-color: #fff;
    border: 1px solid #f2f2f2;
    border-radius: 4px;
    padding: 8px 32px 8px 8px;

    &::after {
      content: "";
      position: absolute;
      width: 20px;
      height: 20px;
      right: 8px;
      top: 6px;
      background: url("@/assets/icons/hit.svg") no-repeat center;
    }
  }

  .discount {
    position: absolute;
    bottom: 12px;
    left: 12px;
    background-color: $accent-color;
    border-radius: 4px;
    padding: 6px 10px;
    color: #fff;
    font-weight: 700;
    line-height: 14px;
  }
}

.title-wrapper {
  display: flex;
  flex-direction: column;
  gap: 8px;

  .brand {
    color: $secondary-text;

    &:hover {
      color: $accent-color;
    }
  }

  .title {
    margin: 0;
    font-weight: 400;
    font-size: 14px;
    line-height: 16px;

    &:hover {
      color: $accent-color;
    }
  }
}

.price-wrapper {
  display: flex;
  gap: 8px;
  align-items: center;
  line-height: 14px;

  .price {
    font-size: 16px;
  }

  .full-price {
    font-size: 12px;
    color: $secondary-text;
    text-decoration: line-through;
  }
}

.button {
  margin-top: auto;
  align-self: start;
  font-weight: 700;
  line-height: 14px;
  color: $accent-color;
  padding: 12px 16px;
  border: 1px solid $accent-color;
  border-radius: 4px;
  transition: all 0.2s ease-in-out;

  &:hover {
    background-color: $accent-color;
    color: #fff;
  }

  &--disabled {
    align-self: stretch;
    text-align: center;
    color: $secondary-text;
    border-color: $secondary-text;
  }
}
</style>
