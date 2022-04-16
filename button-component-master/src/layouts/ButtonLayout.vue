<template>
	<my-button />
	<my-button variant="outline" />
	<my-button variant="text" />
	<my-button disable-shadow />
	<my-button disabled />
	<my-button disabled variant="text" />
</template>
<script>
import MyButton from '@/components/MyButton.vue'
export default {
	components: {
		MyButton
	}
}
</script>
