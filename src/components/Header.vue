<template>
  <div class="Header">
    <h1>{{"The Solar System"}}</h1>
    <hr>
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
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100vw;
  height: 10vh;
  background-color: #07252e;
  font-family: "Cinzel", serif;
  color: #faa533;
}

h1 {
  text-align: center;
  letter-spacing: 1rem;
}

hr {
  height: 5px;
  width: 40%;
  background: #faa533;
  border: none;
  border-radius: 2px;
}
</style>
