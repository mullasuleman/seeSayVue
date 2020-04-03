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
		display: flex;
		justify-content: center;
		flex-wrap: wrap;
		padding: 1rem;
		background: #07252e;
		color: #ebe2d0;
		width: 100vw;
		box-shadow: 0 -5px 100px rgba(235, 226, 208, 0.1);
	}
</style>
