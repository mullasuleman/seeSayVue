<template>
  <div class="Header">
    <h1>SEE&SAY</h1>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: {}
};
</script>

<style scoped>
.Header {
  padding: 1rem;
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
  width: 100vw;
  height: 8vh;
  background-color: #444;
}
</style>
