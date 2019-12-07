<template>
  <div id="App">
    <Header />
    <CardContainer :cardData="planets" />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer";
import CardContainer from "./components/Card-Container.vue";

export default {
  name: "app",
  components: {
    Header,
    CardContainer,
    Footer
  },
  data() {
    return {
      planets: [
        // Need to add rest of planets
        // Make sure images of planets have black BGs for consistency
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
          name: "Saturn",
          source: "Saturn.jpg",
          audio: { name: "", sentence: "" }
        },
        {
          name: "Pluto",
          source: "Pluto.png",
          audio: { name: "", sentence: "" }
        },
        {
          name: "Mercury",
          source: "Mercury.jpg",
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
        },
        {
          name: "Uranus",
          source: "Uranus.jpg",
          audio: { name: "", sentence: "" }
        },
        {
          name: "Venus",
          source: "Venus.jpg",
          audio: { name: "", sentence: "" }
        },
        {
          name: "The Sun",
          source: "Sun.jpg",
          audio: { name: "", sentence: "" }
        }
      ]
    };
  }
};
</script>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
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
