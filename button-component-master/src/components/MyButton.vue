<template>
	<button
		type="button"
		:class="[
			css.button,
			{
				[css.buttonOutline]: variant === 'outline',
				[css.buttonText]: variant === 'text',
				[css.buttonShadowDisabled]: disableShadow,
				[css.buttonDisabled]: disabled,
				[css.buttonTextDisabled]: disabled && variant == 'text'
			}
		]"
	>
		Default
	</button>
</template>
<script>
export default {
	props: {
		variant: {
			type: String,
			default: 'default',
			validator(value) {
				return ['default', 'outline', 'text'].indexOf(value) > -1
			}
		},
		disableShadow: {
			type: Boolean,
			default: false
		},
		disabled: {
			type: Boolean,
			default: false
		}
	}
}
</script>
<style src="./MyButton.css" module="css"></style>
