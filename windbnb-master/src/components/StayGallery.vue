<script setup>
import StayCard from '../components/StayCard.vue'
</script>
<template>
	<div class="wrapper">
		<div class="inner">
			<h2 class="title">Stays in Finland</h2>
			<p class="numbers-stay">12+ stays</p>
		</div>
		<stay-card />
	</div>
</template>
<style scoped>
.wrapper {
	width: calc(100% - 2rem);
	margin-left: auto;
	margin-right: auto;
	display: flex;
	flex-direction: column;
	align-items: center;
	font-family: 'Montserrat';
}
.inner {
	width: inherit;
	display: flex;
	align-items: center;
	justify-content: space-between;
}
.title {
	margin: 0;
	font-weight: 700;
	font-size: 1.8rem;
	color: #333333;
	line-height: 22px;
}
.numbers-stay {
	font-weight: 500;
	font-size: 1.4rem;
	color: #4f4f4f;
}
</style>
