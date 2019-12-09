<template>
  <div id="Card" @click="playAudio(require(`../assets/audios/${audio}`))">
    <img :src="require(`../assets/images/${imgSrc}`)" :alt="name" />
    <h2>{{name}}</h2>
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
    addHistory() {
      if (this.history.length >= 10) {
        this.history.shift();
      }
      this.history.push(this.imgSrc);
    },
    playAudio(file) {
      let audio = new Audio(file);
      audio.play();
      this.addHistory();
    }
  }
};
</script>

<style scoped>
#Card {
  margin: 1rem 0;
  color: #2c3e50;
  height: 17rem;
  width: 15vw;
  border-radius: 1rem;
  box-shadow: 0px 0px 14px 1px rgba(222, 222, 222, 0.2);
  transition: 0.3s ease-out;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  align-items: flex-start;
  overflow: hidden;
}

#Card:hover {
  transform: scale(1.05);
  cursor: pointer;
  border: 3px solid white;
}

img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

h2 {
  position: absolute;
  padding: 1rem;
  color: #fff;
}
</style>
