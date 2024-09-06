<template>
  <div class="header">
    <div class="search-wrapper">
      <a href="#">
        <img src="@/assets/icons/arrow.svg" alt="" />
      </a>
      <input class="search" type="text" placeholder="Запрос" />
      <button class="clear">
        <img src="@/assets/icons/cross.svg" alt="" />
      </button>
      <button type="submit" class="submit">Найти</button>
    </div>
    <div class="divider"></div>
    <h1 class="title">Название категории</h1>
  </div>
</template>

<style scoped lang="scss">
@import "@/assets/variables";

.search-wrapper {
  width: 100%;
  display: flex;
  gap: 16px;
  align-items: center;
  padding: 8px 0;

  .search {
    width: 100%;
    height: 38px;
    font-family: inherit;
    font-size: 16px;
    line-height: 14px;
    border: none;
    flex-grow: 1;

    &::placeholder {
      color: inherit;
    }
  }

  .clear {
    background: none;
    border: none;
    padding: 0;
  }

  .submit {
    height: 38px;
    font-family: inherit;
    font-size: 16px;
    line-height: 14px;
    border: none;
    border-radius: 5px;
    background-color: $accent-color;
    color: #fff;
    padding: 12px 16px;
  }
}

.divider {
  margin-bottom: 12px;
  margin-left: 36px;
  border-top: 1px solid $border-color;
}

.title {
  padding: 0 8px;
  margin: 0;
  font-size: 22px;
  font-weight: 400;
  line-height: 28px;
}
</style>
