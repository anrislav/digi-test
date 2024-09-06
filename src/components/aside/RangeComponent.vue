<script setup>
defineProps(["title"]);
</script>

<template>
  <section class="range">
    <h3 class="title">{{ title }}</h3>
    <div class="from-to">
      <span class="input-wrapper"
        ><input class="input" type="number" name="from" id="from" value="5500"
      /></span>
      <span class="divider"></span>
      <span class="input-wrapper"
        ><input class="input" type="number" name="to" id="to" value="5500"
      /></span>
    </div>
  </section>
</template>
<style scoped lang="scss">
@import "@/assets/variables";

.range {
  display: flex;
  flex-direction: column;
  gap: 16px;
}

.title {
  margin: 0;
  font-size: 16px;
  line-height: 20px;
  font-weight: 700;
  text-align: center;
}

.from-to {
  display: grid;
  grid-template-columns: 1fr 10px 1fr;
  gap: 16px;
  align-items: center;
}

.input-wrapper {
  position: relative;

  &::before {
    position: absolute;
    top: 12px;
    font-size: 12px;
    line-height: 14px;
    content: "от";
    left: 8px;
    color: $secondary-text;
  }

  &::after {
    position: absolute;
    content: "₽";
    top: 11px;
    right: 8px;
  }

  .input {
    width: 100%;
    border: 1px solid $border-color;
    border-radius: 4px;
    font-size: 14px;
    line-height: 16px;
    padding: 10px 20px 10px 26px;

    &::-webkit-outer-spin-button,
    &::-webkit-inner-spin-button {
      -webkit-appearance: none;
      margin: 0;
    }
  }
}

.divider {
  width: 10px;
  height: 1px;
  border-top: 1px solid $border-color;
}
</style>
