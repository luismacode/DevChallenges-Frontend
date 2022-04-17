<template>
	<main class="main">
		<div class="main__inner">
			<h2 class="main__title">Buttons</h2>
			<slot></slot>
		</div>
	</main>
</template>
<style scoped>
.main {
	display: flex;
	justify-content: center;
	align-items: center;
}
.main__inner {
	width: 60%;
	max-width: 1400px;
}
.main__title {
	font-family: 'Poppins', sans-serif;
	font-size: 2.4rem;
	font-weight: 500;
	line-height: 36px;
	color: hsl(0, 0%, 31%);
	margin-bottom: 2em;
}
</style>
