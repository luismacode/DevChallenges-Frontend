<script setup>
import MyInput from '../components/MyInput.vue'
import MyLabel from '../components/MyLabel.vue'
</script>
<template>
	<div class="row">
		<my-label />
		<my-input />
	</div>
	<div class="row">
		<my-label error />
		<my-input error />
	</div>
	<div class="row">
		<my-label />
		<my-input disabled />
	</div>
	<div class="row flex">
		<div class="field">
			<my-label />
			<my-input helper-text="some interesting text" />
		</div>
		<div class="field">
			<my-label error />
			<my-input helper-text="some interesting text" error />
		</div>
	</div>
</template>
<style scoped>
.row {
	margin-bottom: 2em;
}
.flex {
	display: flex;
}
.field {
	margin-right: 2em;
}
</style>
