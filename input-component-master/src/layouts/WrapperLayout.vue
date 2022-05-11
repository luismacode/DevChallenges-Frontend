<template>
	<main class="wrapper">
		<div class="column-20">
			<slot name="logo"></slot>
		</div>
		<div class="column-60">
			<slot name="title"></slot>
			<slot name="body"></slot>
		</div>
	</main>
</template>
<style scoped>
.wrapper {
	width: 96%;
	max-width: 1200px;
	margin-left: auto;
	margin-right: auto;
	padding: 1em;
}
@media screen and (min-width: 576px) {
	.wrapper {
		width: 100%;
		display: flex;
		gap: 2em;
	}
	.column-20 {
		flex-basis: 20%;
	}
	.column-80 {
		flex-basis: 80%;
	}
}
</style>
