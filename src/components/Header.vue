<template>
  <div class="Header">
    <h1>SEE&SAY</h1>
  </div>
</template>

<script>
export default {
  name: "Header",
  components: {},
  props: {
    history: Array
  }
};
</script>

<style scoped>
.Header {
  padding: 0.2rem 8rem;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  width: 100vw;
  height: 10vh;
  background-color: rgb(250, 198, 28);
  font-family: "Cinzel", serif;
  color: #fff;
}
</style>
