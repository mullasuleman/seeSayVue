<template>
	<div id="Footer">
		<FooterSection
			v-for="(credit, index) in credits"
			:key="index"
			:sectionTitle="credit.sectionTitle"
			:items="credit.items"
		/>
	</div>
</template>

<script>
	import FooterSection from "./FooterSection.vue";
	export default {
		name: "Footer",
		components: {
			FooterSection
		},
		props: {
			credits: Array
		}
	};
</script>

<style>
	#Footer {
		color: #ffffff;
		/* height: 8vh; */
		width: 100vw;
		background-color: #333;
	}
</style>
