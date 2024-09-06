<script setup>
import Categories from "./CategoriesComponent.vue";
import Range from "./RangeComponent.vue";
import FilterCheck from "./FilterCheckComponent.vue";
const sizes = [
	{ id: 1, title: "Атрибут", number: 3, checked: false },
	{ id: 2, title: "Атрибут", number: 3, checked: false },
	{ id: 3, title: "Атрибут", number: 3, checked: false },
	{ id: 4, title: "Атрибут", number: 3, checked: false },
	{ id: 5, title: "Атрибут", number: 3, checked: false },
	{ id: 6, title: "Атрибут", number: 3, checked: false },
];
const brands = [
	{ id: 1, title: "Атрибут", number: 3, checked: true },
	{ id: 2, title: "Атрибут", number: 3, checked: false },
	{ id: 3, title: "Атрибут", number: 3, checked: false },
	{ id: 4, title: "Атрибут", number: 3, checked: false },
	{ id: 5, title: "Атрибут", number: 3, checked: false },
	{ id: 6, title: "Атрибут", number: 3, checked: false },
	{ id: 7, title: "Атрибут", number: 3, checked: false },
	{ id: 8, title: "Атрибут", number: 3, checked: false },
];
</script>

<template>
	<aside>
		<Categories></Categories>
		<Range title="Цена"></Range>
		<FilterCheck title="Бренд" :attrs="brands" :isSearch="true"></FilterCheck>
		<FilterCheck title="Размер" :attrs="sizes"></FilterCheck>
	</aside>
</template>

<style scoped lang="scss">
aside {
	flex-shrink: 0;
	display: flex;
	flex-direction: column;
	gap: 28px;
	width: 280px;

	@media screen and (width < 1440px) {
		width: 220px;
	}

	@media screen and (width < 1024px) {
		display: none;
	}
}
</style>
