<script setup>
import Header from "@/components/header/HeaderComponent.vue";
import Aside from "@/components/aside/AsideComponent.vue";
import Main from "@/components/main/MainComponent.vue";
</script>

<template>
	<div id="app">
		<Header></Header>
		<div class="container">
			<Aside></Aside>
			<Main></Main>
		</div>
	</div>
</template>

<style lang="scss">
.container {
	display: flex;
	gap: 36px;
}
</style>
