<template>
	<div class="container">
		<span v-if="startIcon" class="material-symbols-outlined icon icon-left">
			call
		</span>
		<input
			v-if="!multiline"
			id="text"
			:class="{
				inputError: error,
				inputDisabled: disabled,
				inputSizeSm: size === 'sm',
				inputSizeMd: size === 'md',
				fullWidth: fullWidth
			}"
			type="text"
			:placeholder="value"
		/>
		<span v-if="endIcon" class="material-symbols-outlined icon icon-right">
			lock
		</span>
		<textarea v-if="multiline" :rows="row * 2" placeholder="Placeholder" />
	</div>
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
		},
		startIcon: {
			type: Boolean,
			default: false
		},
		endIcon: {
			type: Boolean,
			default: false
		},
		value: {
			type: String,
			default: 'Placeholder'
		},
		size: {
			type: String,
			default: 'md',
			validator(value) {
				return ['sm', 'md'].indexOf(value) > -1
			}
		},
		fullWidth: {
			type: Boolean,
			default: false
		},
		multiline: {
			type: Boolean,
			default: false
		},
		row: {
			type: String,
			default: null
		}
	}
}
</script>
<style scoped>
::placeholder {
	color: hsl(0, 0%, 51%);
}
input,
textarea {
	font-size: 1.4rem;
	font-family: 'NotoSansJP', sans-serif;
	font-weight: 500;
	border-radius: 12px;
}
input {
	display: block;
	width: 200px;
	outline: none;
	border: 1px solid #828282;
	padding-left: 1em;
}
textarea {
	padding: 1em;
}
.fullWidth {
	width: 100%;
}
.inputSizeSm {
	height: 40px;
}
.inputSizeMd {
	height: 56px;
}
.container {
	position: relative;
}
.icon {
	position: absolute;
	color: #828282;
}
.icon-left {
	left: 0.2em;
	top: 0.7em;
}
.icon-left + input::placeholder {
	padding-left: 1.5em;
}
.icon-right {
	right: 0.2em;
	top: 0.7em;
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
.inputError,
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
	input:hover,
	textarea:hover {
		border-color: hsl(0, 0%, 20%);
	}
	.inputDisabled:hover {
		border-color: hsl(0, 0%, 88%);
		cursor: no-drop;
	}
	.inputError:hover {
		border-color: hsl(0, 51%, 64%);
	}
}
</style>
