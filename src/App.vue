<template>
	<div id="App">
		<Header :history="history" />
		<CardContainer :cardData="planets" :history="history" />
		<HistoryBar :history="history" />
		<Footer />
	</div>
</template>

<script>
	import Header from "./components/Header.vue";
	import Footer from "./components/Footer";
	import HistoryBar from "./components/HistoryBar";
	import CardContainer from "./components/Card-Container.vue";

	export default {
		name: "app",
		components: {
			Header,
			CardContainer,
			HistoryBar,
			Footer
		},
		data() {
			return {
				planets: [
					{
						name: "The Sun",
						source: "Sun.jpg",
						audio: { name: "", sentence: "" }
					},
					{
						name: "Mercury",
						source: "Mercury.jpg",
						audio: { name: "", sentence: "" }
					},
					{
						name: "Venus",
						source: "Venus.jpg",
						audio: { name: "", sentence: "" }
					},
					{
						name: "Earth",
						source: "Earth.png",
						audio: { name: "", sentence: "" }
					},
					{
						name: "Mars",
						source: "Mars.jpg",
						audio: { name: "", sentence: "" }
					},
					{
						name: "Jupiter",
						source: "Jupiter.jpg",
						audio: { name: "", sentence: "" }
					},
					{
						name: "Saturn",
						source: "Saturn.jpg",
						audio: { name: "", sentence: "" }
					},
					{
						name: "Uranus",
						source: "Uranus.jpg",
						audio: { name: "", sentence: "" }
					},
					{
						name: "Neptune",
						source: "Neptune.jpg",
						audio: { name: "", sentence: "" }
					},
					{
						name: "Pluto",
						source: "Pluto.png",
						audio: { name: "", sentence: "" }
					}
				],
				history: []
			};
		}
	};
</script>

<style>
	* {
		padding: 0;
		margin: 0;
		box-sizing: border-box;
		user-select: none;
		font-family: sans-serif;
	}

	#App {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		align-items: center;
		color: #2c3e50;
		min-height: 100vh;
		width: 100vw;
		background: linear-gradient(
			180deg,
			rgba(36, 35, 48, 1) 0%,
			rgba(87, 66, 94, 1) 100%
		);
	}
</style>
