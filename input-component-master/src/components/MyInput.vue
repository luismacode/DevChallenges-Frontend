<template>
	<input id="text" type="text" placeholder="Placeholder" />
</template>
<style scoped>
::placeholder {
	color: hsl(0, 0%, 51%);
}
input {
	display: block;
	width: 200px;
	height: 56px;
	font-size: 1.4rem;
	font-family: 'NotoSansJP', sans-serif;
	font-weight: 500;
	border-radius: 12px;
	outline: none;
	border: 1px solid #828282;
	padding-left: 1em;
}
input:focus {
	border-color: hsl(224, 100%, 58%);
}
@media (hover: hover) {
	input:hover {
		border-color: hsl(0, 0%, 20%);
	}
}
</style>
