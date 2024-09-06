<template>
  <ul class="list">
    <li>
      <a href="#" class="item">
        <span class="title">Название категории</span>
        <span class="number">3</span>
      </a>
      <ul class="list sub-list">
        <li>
          <a href="#" class="item">
            <span class="title">Название категории</span>
            <span class="number">3</span>
          </a>
        </li>
        <li>
          <a href="#" class="item">
            <span class="title">Название категории</span>
            <span class="number">3</span>
          </a>
        </li>
        <li>
          <a href="#" class="item item--active">
            <span class="title">Название категории</span>
            <span class="number">3</span>
          </a>
        </li>
      </ul>
    </li>
  </ul>
</template>
<style scoped lang="scss">
@import "@/assets/variables";

.list {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

.item {
  display: grid;
  grid-template-columns: 1fr auto;
  justify-content: space-between;
  padding: 7px 16px 7px 8px;
  border-radius: 5px;
  text-decoration: none;
  color: inherit;

  &--active {
    background-color: $background-hover;
    pointer-events: none;
  }

  &:hover {
    color: $accent-color;
  }
}

.number {
  text-align: right;
  font-size: 12px;
  line-height: 14px;
  color: $secondary-text;
}

.sub-list {
  .item {
    padding-left: 32px;
  }
}
</style>
