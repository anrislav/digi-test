<script setup>
defineProps(["title", "attrs", "isSearch"]);
</script>
<template>
  <section class="filter">
    <h3 class="title search" v-if="isSearch">
      {{ title }} <button class="clear">Очистить</button>
    </h3>
    <h3 class="title" v-else>{{ title }}</h3>

    <div class="search-wrapper" v-if="isSearch">
      <input
        class="search"
        type="text"
        name="brand-search"
        placeholder="Поиск"
      />
    </div>

    <ul class="list">
      <li :key="attr.id" v-for="attr of attrs">
        <label class="item">
          <input
            class="input-checkbox"
            type="checkbox"
            :checked="attr.checked"
          />
          <div class="checkbox"></div>
          <span class="attribute">{{ attr.title }}</span>
          <span class="number">{{ attr.number }}</span>
        </label>
      </li>
    </ul>
  </section>
</template>
<style scoped lang="scss">
@import "@/assets/variables";

.filter {
  display: flex;
  flex-direction: column;
  gap: 16px;
}

.title {
  display: flex;
  margin: 0;
  font-size: 16px;
  line-height: 20px;
  font-weight: 700;
  justify-content: center;
  align-items: center;

  &.search {
    justify-content: space-between;
  }

  .clear {
    border: none;
    background-color: #fff;
    text-decoration: underline;
    color: $secondary-text;
    cursor: pointer;
    font-family: inherit;
    font-size: 12px;
    line-height: 12px;

    &:hover {
      color: $primary-text;
    }
  }
}

.search-wrapper {
  width: 100%;
  position: relative;

  &::before {
    content: "";
    position: absolute;
    width: 16px;
    height: 16px;
    top: 12px;
    left: 12px;
    background: url("@/assets/icons/search-small.svg") no-repeat center;
  }

  .search {
    width: 100%;
    border: 1px solid $border-color;
    border-radius: 4px;
    padding: 10px 10px 10px 36px;
    font-size: 14px;
    line-height: 16px;

    &::placeholder {
      color: $secondary-text;
    }
  }
}

.list {
  margin: 0;
  padding: 0;
  list-style-type: none;
  display: flex;
  flex-direction: column;
  gap: 12px;
  max-height: 180px;
  overflow: scroll;
}

.item {
  display: flex;
  gap: 12px;
  cursor: pointer;
  align-items: center;

  .checkbox {
    height: 20px;
    width: 20px;
    border-radius: 3px;
    border: 1px solid $border-color;
  }

  .attribute {
    flex-grow: 1;
  }

  &:hover .title {
    color: $accent-color;
  }

  &:hover .checkbox {
    border: 1px solid $accent-color;
  }

  .number {
    color: $secondary-text;
    font-size: 12px;
    line-height: 14px;
    margin-right: 16px;
  }

  .input-checkbox {
    position: absolute;
    z-index: -1;
    opacity: 0;

    &:checked ~ .checkbox {
      position: relative;
      background-color: $accent-color;
      border-color: $accent-color;

      &::before {
        content: "";
        position: absolute;
        width: 20px;
        height: 20px;
        top: -1px;
        left: -1px;
        background: url("@/assets/icons/check.svg") no-repeat center;
      }
    }
  }
}
</style>
