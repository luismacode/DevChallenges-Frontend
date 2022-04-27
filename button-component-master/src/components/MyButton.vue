<template>
	<button
		type="button"
		:class="[
			css.button,
			{
				[css.outlinedButton]: variant === 'outline',
				[css.outlinedPrimaryButton]:
					variant === 'outline' && color === 'primary',
				[css.outlinedSecondaryButton]:
					variant === 'outline' && color === 'secondary',
				[css.outlinedDangerButton]: variant === 'outline' && color === 'danger',
				[css.textButton]: variant === 'text',
				[css.textPrimaryButton]: variant === 'text' && color === 'primary',
				[css.textSecondaryButton]: variant === 'text' && color === 'secondary',
				[css.textDangerButton]: variant === 'text' && color === 'danger',
				[css.buttonShadowDisabled]: disableShadow,
				[css.buttonDisabled]: disabled,
				[css.buttonTextDisabled]: disabled && variant == 'text',
				[css.buttonIcons]: startIcon || endIcon,
				[css.buttonSm]: size === 'sm',
				[css.buttonMd]: size === 'md',
				[css.buttonLg]: size === 'lg',
				[css.buttonPrimary]: color === 'primary',
				[css.buttonSecondary]: color === 'secondary',
				[css.buttonDanger]: color === 'danger'
			}
		]"
	>
		<span v-if="startIcon" class="material-icons md-18">{{ startIcon }}</span>
		<slot></slot>
		<span v-if="endIcon" class="material-icons md-18">{{ endIcon }}</span>
	</button>
</template>
<script>
export default {
	props: {
		variant: {
			type: String,
			default: null,
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
		},
		startIcon: {
			type: String,
			default: null
		},
		endIcon: {
			type: String,
			default: null
		},
		size: {
			type: String,
			default: null,
			validator(value) {
				return ['sm', 'md', 'lg'].indexOf(value) > -1
			}
		},
		color: {
			type: String,
			default: null,
			validator(value) {
				return ['default', 'primary', 'secondary', 'danger']
			}
		}
	}
}
</script>
<style src="./MyButton.css" module="css"></style>
