<template>
	<main class="wrapper">
		<div class="column-20">
			<div class="logo-container">
				<slot name="logo"></slot>
			</div>
		</div>
		<div class="column-60">
			<slot name="title"></slot>
			<slot name="body"></slot>
			<slot name="footer"></slot>
		</div>
	</main>
</template>
<style scoped>
.wrapper {
	max-width: 1200px;
	margin-left: 2em;
	padding: 5em 0 0 4em;
}
.logo-container {
	width: 120px;
}
@media screen and (min-width: 576px) {
	.wrapper {
		display: flex;
		gap: 5em;
	}
	.column-20 {
		flex-basis: 10%;
	}
	.column-80 {
		flex-basis: 90%;
	}
}
</style>
