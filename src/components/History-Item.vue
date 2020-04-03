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
  box-shadow: 0px 0px 14px 1px rgba(222, 222, 222, 0.2);
  transform: scale(0.95);
  cursor: pointer;
}

img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
