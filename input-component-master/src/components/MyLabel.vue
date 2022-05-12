<template>
	<label for="text" :class="{ labelError: error }">Label</label>
</template>
<script>
export default {
	props: {
		error: {
			type: Boolean,
			default: false
		}
	}
}
</script>
<style scoped>
label {
	display: block;
	font-size: 1.2rem;
	line-height: 17px;
	font-family: 'NotoSansJP';
	font-weight: 400;
	color: hsl(0, 0%, 20%);
	margin-bottom: 0.3em;
}
.labelError {
	color: hsl(0, 65%, 51%);
}
label:hover {
	cursor: pointer;
}
</style>
