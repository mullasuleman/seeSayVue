<template>
  <div id="App">
    <Header :title="title" :intro="intro" />
    <CardContainer :cardData="planets" :history="history" />
    <HistoryBar :history="history" />
    <Footer :credits="credits" />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
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
      title: "The Solar System",
      intro:
        "A See 'N Say experience created for 3-6 years old. \nClick any card to learn about our solar system and planets!",
      planets: [
        {
          name: "The Sun",
          source: "Sun.jpg",
          audio: "Sun.mp3",
          desc: "The Sun is the star at the centre of the Solar System."
        },
        {
          name: "Mercury",
          source: "Mercury.jpg",
          audio: "Mercury.mp3",
          desc: "Mercury is the first planet from the Sun."
        },
        {
          name: "Venus",
          source: "Venus.jpg",
          audio: "Venus.mp3",
          desc: "Venus is the second planet from the Sun."
        },
        {
          name: "Earth",
          source: "Earth.png",
          audio: "Earth.mp3",
          desc: "Earth is our home. It is the third planet from the Sun."
        },
        {
          name: "Mars",
          source: "Mars.jpg",
          audio: "Mars.mp3",
          desc: "Mars is the fourth planet from the Sun."
        },
        {
          name: "Jupiter",
          source: "Jupiter.jpg",
          audio: "Jupiter.mp3",
          desc: "Jupiter is the largest and fifth planet from the Sun."
        },
        {
          name: "Saturn",
          source: "Saturn.jpg",
          audio: "Saturn.mp3",
          desc: "Saturn is the sixth planet from the Sun."
        },
        {
          name: "Uranus",
          source: "Uranus.jpg",
          audio: "Uranus.mp3",
          desc: "Uranus is the seventh planet from the Sun."
        },
        {
          name: "Neptune",
          source: "Neptune.jpg",
          audio: "Neptune.mp3",
          desc: "Neptune is the eighth planet from the Sun."
        },
        {
          name: "Pluto",
          source: "Pluto.png",
          audio: "Pluto.mp3",
          desc: "Pluto is the largest dwarf planet in the solar system."
        }
      ],
      history: [],
      credits: [
        {
          sectionTitle: "Fonts",
          items: ["Google Fonts fonts.google.com"]
        },
        {
          sectionTitle: "Audio",
          items: ["Notevibes www.notevibes.com"]
        },
        {
          sectionTitle: "Group Members",
          items: ["Michael Mueller", "Suleman Mulla", "Usman Butt"]
        },
        {
          sectionTitle: "Images",
          items: ["NASA solarsystem.nasa.gov"]
        },
        {
          sectionTitle: "Information",
          items: ["NASA solarsystem.nasa.gov"]
        }
      ]
    };
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Cinzel&display=swap");
@import url("https://fonts.googleapis.com/css?family=Rajdhani:400,600&display=swap");

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
  min-height: 100vh;
  width: 100vw;
  background-image: url("../src/assets/images/space_bg.jpg");
  background-size: cover;
  background-attachment: fixed;
  background-repeat: no-repeat;
}
</style>
