<template>
  <div id="HistoryItem" @click="playAudio">
    <img :src="require(`../assets/images/${imgSrc}`)" alt="planet" />
  </div>
</template>

<script>
export default {
  name: "HistoryItem",
  props: {
    imgSrc: String,
    audioSrc: String
  },
  methods: {
    playAudio() {
      window.console.log(this.audioSrc)
      let file = require(`../assets/audios/${this.audioSrc}`);
      let audio = new Audio(file);
      audio.play();
    }
  },
};
</script>

<style>
#HistoryItem {
  height: 100%;
  width: 9%;
  background-color: rgba(212, 212, 212, 0.295);
  border-radius: 1rem;
  transition: 0.2s ease-in;
  overflow: hidden;
  margin: 0 0.5%;
}

#HistoryItem:hover {
  background-color: rgba(212, 212, 212, 0.678);
  transform: scale(1.1);
  cursor: pointer;
}

img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
