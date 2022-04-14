<script setup>
import Button from '@/components/Button.vue'
</script>
<template>
	<header :class="css.header">
		<h1 :class="css.header__title">Devchallenges.io</h1>
	</header>
	<main :class="css.main">
		<div :class="css.main__inner">
			<h2 :class="css.main__title">Buttons</h2>
			<Button />
		</div>
	</main>
</template>
<style src="./ButtonsPage.css" module="css"></style>
