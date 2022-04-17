<script setup>
import ButtonLayout from '@/layouts/ButtonLayout.vue'
import FooterLayout from '@/layouts/FooterLayout.vue'
import HeaderLayout from '@/layouts/HeaderLayout.vue'
import MainLayout from '@/layouts/MainLayout.vue'
</script>
<template>
	<div class="wrapper">
		<header-layout />
		<main-layout>
			<button-layout />
		</main-layout>
		<footer-layout />
	</div>
</template>
<style scoped>
.wrapper {
	display: flex;
	flex-direction: column;
	min-height: 100vh;
}
</style>
