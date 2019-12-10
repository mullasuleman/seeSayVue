<template>
  <div id="Card" @click="openCard">
    <img :src="require(`../assets/images/${imgSrc}`)" :alt="name" />
    <h2>{{name}}</h2>
    <p>{{desc}}</p>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    imgSrc: String,
    name: String,
    history: Array,
    audio: String,
    desc: String
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
      let file = require(`../assets/audios/${this.audio}`);
      let audio = new Audio(file);
      audio.play();
    }
  }
};
</script>

<style scoped>
#Card {
  margin: 2rem 0;
  color: #2c3e50;
  height: 22rem;
  width: 15vw;
  border-radius: 1rem;
  box-shadow: 0px 0px 14px 1px rgba(222, 222, 222, 0.2);
  transition: 0.3s ease-out;
  overflow: hidden;
  background: #ebe2d0;
  border: 1px solid #07252e;
  animation: init 1s infinite alternate ease-in-out;
}

@keyframes init {
  from {
    border: 1px solid #07252e;
  }
  to {
    border-bottom: 1px solid #ebe2d0;
  }
}

#Card:hover {
  transform: scale(1.05);
  cursor: pointer;
  border: 3px solid #ebe2d0;
  animation: none;
}

#Card:hover > img {
  height: 82%;
}

img {
  align-self: center;
  position: relative;
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 0.9rem;
  transition: 0.5s ease-in-out;
  box-shadow: 0 0 10px #2c3e50;
}

h2 {
  position: relative;
  top: -4rem;
  color: #ebe2d0;
  padding: 1rem;
  text-align: center;
  font-family: "Rajdhani", sans-serif;
  font-weight: 700;
}

p {
  position: relative;
  top: -3.25rem;
  margin: 0 1rem;
  color: #07252e;
  text-align: center;
  font-family: "Rajdhani", sans-serif;
  font-weight: 400;
}
</style>
