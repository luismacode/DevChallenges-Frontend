<template>
	<form>
		<label class="label" for="search">
			<input
				id="search"
				class="search"
				type="search"
				placeholder="Helsinki, Finland"
			/>
			<span class="search-text">Add guests</span>
			<button type="button" class="button">
				<img
					class="search-icon"
					src="../assets/icons/search.svg"
					alt="search icon"
				/>
			</button>
		</label>
	</form>
</template>
<style scoped>
form {
	width: 100%;
	font-family: Mulish;
}
.label {
	display: block;
	width: 297px;
	position: relative;
	margin-left: auto;
	margin-right: auto;
}
.search {
	font-size: 1.4rem;
	font-weight: 400;
	font-family: inherit;
	border: none;
	border-radius: 1rem;
	width: 100%;
	height: 55px;
	box-shadow: 0px 1px 6px 0px hsla(0, 0%, 0%, 0.102);
	padding-left: 1.3em;
}
.search-text {
	top: 2rem;
	right: 20%;
	font-size: 1.4rem;
	font-weight: 400;
	color: #bdbdbd;
	position: absolute;
}
.button {
	top: 1.5rem;
	right: 5%;
	position: absolute;
	background-color: transparent;
	border: none;
	display: flex;
	align-items: center;
	justify-content: center;
}
.search-icon {
	width: 22px;
	height: 22px;
}
</style>
