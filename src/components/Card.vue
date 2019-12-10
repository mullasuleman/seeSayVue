<template>
  <div id="Card" @click="openCard">
    <img :src="require(`../assets/images/${imgSrc}`)" :alt="name" />
    <h2>{{name}}</h2>
    <!-- <p>This is where the text goes</p> -->
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    imgSrc: String,
    name: String,
    history: Array,
    audio: String
  },
  methods: {
    openCard() {
      this.addHistory();
      this.playAudio();
    },
    addHistory() {
      let cardObj = { 
        source: this.imgSrc,
        audio: this.audio
      };
      if (this.history.length >= 10) {
        this.history.shift();
      }
      this.history.push(cardObj);
    },
    playAudio() {
      let file = require(`../assets/audios/${this.audio}`)
      let audio = new Audio(file);
      audio.play();
    }
  }
};
</script>

<style scoped>
#Card {
  margin: 1rem 0;
  color: #2c3e50;
  /* height: 25rem; */
  width: 15vw;
  border-radius: 1rem;
  box-shadow: 0px 0px 14px 1px rgba(222, 222, 222, 0.2);
  transition: 0.3s ease-out;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  align-items: flex-start;
  overflow: hidden;
  background: #ebe2d0;
}

#Card:hover {
  transform: scale(1.05);
  cursor: pointer;
  border: 3px solid white;
}

img {
  align-self: center;
  position: relative;
  width: 150%;
  height: 150%;
  object-fit: cover;
}

h2 {
  position: absolute;
  color: #ebe2d0;
  padding: 1rem;
  font-family: "Rajdhani", sans-serif;
}

p {
  /* position: absolute; */
  margin: 0 1rem;
  background: white;
}
</style>
