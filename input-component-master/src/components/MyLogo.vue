<template>
	<h1 class="logo">Devchallenges.io</h1>
</template>
<style scoped>
.logo {
	font-size: 1.3rem;
	line-height: 20px;
	font-family: 'Poppins', sans-serif;
	font-weight: 600;
	background-image: linear-gradient(
		90deg,
		hsl(11, 93%, 57%) 1%,
		hsl(0, 0%, 31%) 2%
	);
	background-clip: text;
	-webkit-background-clip: text;
	color: transparent;
}
@media screen and (min-width: 576px) {
	.logo {
		background-image: linear-gradient(
			90deg,
			hsl(11, 93%, 57%) 19%,
			hsl(0, 0%, 31%) 20%
		);
	}
}
</style>
