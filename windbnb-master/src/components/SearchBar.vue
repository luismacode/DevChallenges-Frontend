<template>
	<div class="wrapper">
		<div class="inner">
			<div class="content">
				<span class="search-place">Helsinki, Finland</span>
				<span class="search-guest">Add guests</span>
			</div>
			<button type="button" class="button" @click.prevent="isOpen = true">
				<img
					class="search-icon"
					src="../assets/icons/search.svg"
					alt="search icon"
				/>
			</button>
		</div>
	</div>
	<div v-if="isOpen" v-bind="isOpen">
		<search-edition @close="closeEdition(cerrar)" />
	</div>
</template>
<script>
import SearchEdition from './SearchEdition.vue'
export default {
	components: {
		SearchEdition
	},
	data() {
		return {
			isOpen: false
		}
	},
	methods: {
		closeEdition(cerrar) {
			return (this.isOpen = cerrar)
		}
	}
}
</script>
<style scoped>
.wrapper {
	width: 100%;
	font-family: Mulish;
}
.inner {
	display: flex;
	width: 298px;
	margin-left: auto;
	margin-right: auto;
	border-radius: 1rem;
	box-shadow: 0px 1px 6px 0px hsla(0, 0%, 0%, 0.102);
	height: 55px;
}
.content {
	width: 80%;
	display: flex;
	align-items: center;
	justify-content: space-between;
}
.search-place {
	font-size: 1.4rem;
	font-weight: 400;
	padding-left: 1.3em;
}
.search-guest {
	font-size: 1.4rem;
	font-weight: 400;
	color: #bdbdbd;
}
.button {
	width: 20%;
	background-color: transparent;
	border: none;
	outline: none;
	display: flex;
	align-items: center;
	justify-content: center;
}
.search-icon {
	width: 22px;
	height: 22px;
}
</style>
