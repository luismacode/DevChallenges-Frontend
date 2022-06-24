<script setup>
import { computed } from 'vue'
import stays from '../data/stays.json'
const stayList = computed(() => {
	return stays.map(stay => stay)
})
</script>
<template>
	<article v-for="stay in stayList" :key="stay.title" class="card">
		<img :title="stay.title" :src="stay.photo" class="image" />
		<div class="inner">
			<div class="subinner">
				<p v-if="stay.superHost" class="tag">super host</p>
				<p class="type">{{ stay.type }}</p>
				<p>{{ stay.beds }} beds</p>
			</div>
			<p class="rating">
				<img class="star" src="../assets/icons/star.svg" alt="star" />
				<span class="number">{{ stay.rating }}</span>
			</p>
		</div>
		<h3 class="title">{{ stay.title }}</h3>
	</article>
</template>
<style scoped>
.card {
	width: calc(100% - 2rem);
	margin-left: auto;
	margin-left: auto;
	margin-left: 0;
	font-family: 'Montserrat';
}
.image {
	width: 100%;
	height: 240px;
	object-fit: cover;
}
.inner {
	display: flex;
	align-items: center;
	justify-content: space-between;
}
.subinner {
	display: flex;
	align-items: center;
	font-size: 1.2rem;
	font-weight: 500;
	color: #828282;
}
.tag {
	width: 89px;
	height: 25px;
	font-size: 1rem;
	font-weight: 700;
	text-transform: uppercase;
	border: 1px solid #4f4f4f;
	border-radius: 12px;
	display: flex;
	align-items: center;
	justify-content: center;
	color: #4f4f4f;
}
.tag,
.type {
	margin-right: 1rem;
}
.rating {
	display: flex;
	align-items: center;
	font-size: 1.2rem;
	font-weight: 500;
	color: #4f4f4f;
}
.star {
	width: 16px;
	height: 16px;
	margin-right: 0.5em;
}
.title {
	margin-top: 0;
	font-size: 1.4rem;
	font-weight: 600;
	color: #333333;
	line-height: 17px;
}
</style>
