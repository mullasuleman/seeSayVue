<template>
  <div id="Card">
    <img :src="require(`../assets/images/${imgSrc}`)" alt="planets" />
    <h2>{{name}}</h2>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    imgSrc: String,
    name: String
  }
};
</script>

<style scoped>
#Card {
  color: #2c3e50;
  height: 270px;
  width: 200px;
  border-radius: 1rem;
  box-shadow: 0px 0px 14px 1px rgba(0, 0, 0, 0.6);
  transition: 0.3s ease-in;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: left;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  align-items: flex-start;
  overflow: hidden;
}

#Card:hover {
  transform: scale(1.1);
  cursor: pointer;
  border: 3px solid white;
}

img {
  width: auto;
  height: 100%;
}

h2 {
  position: absolute;
  padding: 1rem;
  color: #fff;
}
</style>
