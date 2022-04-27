<template>
	<div class="row">
		<my-button>Default</my-button>
	</div>
	<div class="row">
		<div class="column">
			<my-button variant="outline" color="danger">Default</my-button>
		</div>
		<div class="column">
			<my-button variant="text" color="primary">Default</my-button>
		</div>
	</div>
	<div class="row">
		<my-button disable-shadow>Default</my-button>
	</div>
	<div class="row">
		<div class="column">
			<my-button disabled>Disabled</my-button>
		</div>
		<div class="column">
			<my-button variant="text" disabled>Disabled</my-button>
		</div>
	</div>
	<div class="row">
		<div class="column">
			<my-button color="danger" start-icon="local_grocery_store"
				>Default</my-button
			>
		</div>
		<div class="column">
			<my-button color="primary" end-icon="local_grocery_store"
				>Default</my-button
			>
		</div>
		<div class="column">
			<my-button color="secondary" start-icon="arrow_circle_left"
				>Default</my-button
			>
		</div>
		<div class="column">
			<my-button end-icon="arrow_circle_right">Default</my-button>
		</div>
		<div class="column">
			<my-button start-icon="phone">Default</my-button>
		</div>
		<div class="column">
			<my-button end-icon="send">Default</my-button>
		</div>
		<div class="column">
			<my-button start-icon="local_shipping">Default</my-button>
		</div>
		<div class="column">
			<my-button end-icon="download">Default</my-button>
		</div>
	</div>
	<div class="row">
		<div class="column">
			<my-button size="sm">Default</my-button>
		</div>
		<div class="column">
			<my-button size="md">Default</my-button>
		</div>
		<div class="column">
			<my-button size="lg">Default</my-button>
		</div>
	</div>
	<div class="row">
		<div class="column">
			<my-button>Default</my-button>
		</div>
		<div class="column">
			<my-button color="primary">Default</my-button>
		</div>
		<div class="column">
			<my-button color="secondary">Default</my-button>
		</div>
		<div class="column">
			<my-button color="danger">Default</my-button>
		</div>
	</div>
</template>
<script>
import MyButton from '@/components/MyButton.vue'
export default {
	components: {
		MyButton
	}
}
</script>
<style scoped>
.row {
	display: flex;
	margin-bottom: 4em;
	gap: 1em;
	align-items: center;
	flex-wrap: wrap;
}
.column {
	margin-right: 3em;
}
</style>
