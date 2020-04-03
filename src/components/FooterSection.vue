<template>
	<div class="FooterSection">
		<h3>{{sectionTitle}}</h3>
		<ul>
			<li v-for="(item, index) in items" :key="index">{{ item }}</li>
		</ul>
	</div>
</template>

<script>
	export default {
		name: "FooterSection",
		props: {
			sectionTitle: String,
			items: Array
		}
	};
</script>

<style scoped>
.FooterSection {
	padding: 0.2rem 3rem;
	width: 20%;
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	border-right: 1px solid #faa533;
}

.FooterSection:last-child {
	border-right: none;
}

h3 {
	font-family: "Cinzel", serif;
	color: #faa533;
	letter-spacing: 2px;
	margin-bottom: 0.5rem;
}

ul {
	list-style: none;
	text-align: center;
	font-family: "Rajdhani", sans-serif;
	letter-spacing: 1px;
}
</style>