<template>
	<input
		id="text"
		:class="{ inputError: error, inputDisabled: disabled }"
		type="text"
		placeholder="Placeholder"
	/>
	<span
		v-if="helperText"
		class="helperText"
		:class="{ helperTextError: error }"
		>{{ helperText }}</span
	>
</template>
<script>
export default {
	props: {
		error: {
			type: Boolean,
			default: false
		},
		helperText: {
			type: String,
			default: null
		},
		disabled: {
			type: Boolean,
			default: false
		}
	}
	// data() {
	// 	return {
	// 		hasText
	// 	}
	// }
}
</script>
<style scoped>
::placeholder {
	color: hsl(0, 0%, 51%);
}
input {
	display: block;
	width: 200px;
	height: 56px;
	font-size: 1.4rem;
	font-family: 'NotoSansJP', sans-serif;
	font-weight: 500;
	border-radius: 12px;
	outline: none;
	border: 1px solid #828282;
	padding-left: 1em;
}
.helperText {
	display: inline-block;
	margin-top: 0.4em;
	font-size: 1rem;
	font-family: 'NotoSansJP', sans-serif;
	color: hsl(0, 0%, 51%);
}
.helperTextError {
	color: hsl(0, 65%, 51%);
}
.inputError {
	border-color: hsl(0, 65%, 51%);
}
.inputError:focus {
	border-color: hsl(0, 65%, 51%);
}
.inputDisabled {
	background-color: hsl(0, 0%, 95%);
	border-color: hsl(0, 0%, 88%);
}
input:focus {
	border-color: hsl(224, 100%, 58%);
}
.inputDisabled:focus {
	border-color: none;
}
@media (hover: hover) {
	input:hover {
		border-color: hsl(0, 0%, 20%);
	}
	.inputDisabled:hover {
		border-color: hsl(0, 0%, 88%);
		cursor: no-drop;
	}
}
</style>
