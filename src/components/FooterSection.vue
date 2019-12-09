<template>
	<div>
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
</style>