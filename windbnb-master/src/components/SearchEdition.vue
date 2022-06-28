<template>
	<section class="wrapper">
		<div class="content">
			<div class="header">
				<h4 class="title">Edit your search</h4>
				<img src="../assets/icons/close.svg" alt="close" class="icon-close" />
			</div>
			<form class="form">
				<div class="field">
					<label for="place" class="label">location</label>
					<input id="place" class="input" placeholder="Helsinki,Finland" />
				</div>
				<div class="field">
					<label for="guest" class="label">guests</label>
					<input id="guest" class="input text-light" placeholder="Add guest" />
				</div>
			</form>
			<ul class="list">
				<li class="item">
					<img
						src="../assets/icons/place.svg"
						alt="location"
						class="icon-place"
					/>
					<p class="text">Helsinki,Finland</p>
				</li>
				<li class="item">
					<img
						src="../assets/icons/place.svg"
						alt="location"
						class="icon-place"
					/>
					<p class="text">Turku,Finland</p>
				</li>
				<li class="item">
					<img
						src="../assets/icons/place.svg"
						alt="location"
						class="icon-place"
					/>
					<p class="text">Oulu,Finland</p>
				</li>
				<li class="item">
					<img
						src="../assets/icons/place.svg"
						alt="location"
						class="icon-place"
					/>
					<p class="text">Vaasa,Finland</p>
				</li>
			</ul>
			<button type="button" class="button button-theme">
				<img
					src="../assets/icons/search-alt.svg"
					class="icon-search"
					alt="icon-search"
				/>
				<span>Search</span>
			</button>
		</div>
	</section>
</template>
<script>
export default {}
</script>
<style scoped>
.wrapper {
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
}
.content {
	width: calc(100% - 2.2rem);
	margin: auto;
	background-color: #ffffff;
	height: 630px;
	font-family: 'Mulish';
}
.header {
	display: flex;
	align-items: center;
	justify-content: space-between;
}
.title {
	font-size: 1.2rem;
	font-weight: 700;
	color: #333333;
}
.icon-close {
	width: 20px;
	height: 20px;
}
.form {
	height: 113px;
	box-shadow: 0px 1px 6px 0px #0000001a;
	border-radius: 16px;
}
form div:nth-of-type(1) {
	border-bottom-width: 1px;
	border-bottom-style: solid;
	border-bottom-color: #f2f2f2;
}
.field {
	display: flex;
	flex-direction: column;
	justify-content: center;
	gap: 0.6em;
	padding: 0 2.5em;
	height: 56px;
}
.label {
	display: block;
	font-size: 0.9rem;
	font-weight: 800;
	color: #333333;
	text-transform: uppercase;
}
.input {
	border: none;
	padding-left: 0;
	font-weight: 400;
	font-size: 1.4rem;
}
.text-light {
	color: #bdbdbd;
}
.list {
	list-style: none;
	padding-left: 2em;
}
.item {
	display: flex;
	color: #4f4f4f;
}
.text {
	font-size: 1.4rem;
	font-weight: 400;
}
.icon-place {
	margin-right: 0.9em;
}
.button {
	position: absolute;
	bottom: 0;
	left: 50%;
	transform: translate(-50%, 0);
	display: flex;
	align-items: center;
	font-family: 'Mulish';
	background-color: #eb5757e5;
	border: none;
	border-radius: 16px;
	height: 48px;
	padding: 0 2em;
	color: #fff;
	gap: 1rem;
	margin-bottom: 2em;
}
.button span {
	font-size: 1.4rem;
	font-weight: 700;
}
</style>
