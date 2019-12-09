<template>
  <div id="App">
    <Header />
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
          audio: "Sun.mp3"
        },
        {
          name: "Mercury",
          source: "Mercury.jpg",
          audio: "Mercury.mp3"
        },
        {
          name: "Venus",
          source: "Venus.jpg",
          audio: "Venus.mp3"
        },
        {
          name: "Earth",
          source: "Earth.png",
          audio: "Earth.mp3"
        },
        {
          name: "Mars",
          source: "Mars.jpg",
          audio: "Mars.mp3"
        },
        {
          name: "Jupiter",
          source: "Jupiter.jpg",
          audio: "Jupiter.mp3"
        },
        {
          name: "Saturn",
          source: "Saturn.jpg",
          audio: "Saturn.mp3"
        },
        {
          name: "Uranus",
          source: "Uranus.jpg",
          audio: "Uranus.mp3"
        },
        {
          name: "Neptune",
          source: "Neptune.jpg",
          audio: "Neptune.mp3"
        },
        {
          name: "Pluto",
          source: "Pluto.png",
          audio: "Pluto.mp3"
        }
      ],
      history: []
    };
  }
};
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Cinzel&display=swap');

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  user-select: none;
}

body {
  overflow-x: hidden;
}

#App {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  color: #2c3e50;
  min-height: 100vh;
  width: 100vw;
  background-image: url("../src/assets/images/space_bg.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
</style>
