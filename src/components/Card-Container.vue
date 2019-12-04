<template>
  <div id="CardContainer">
    <!-- Cards are just here temporarily for testing -->
    <Card />
    <Card />
    <Card />
  </div>
</template>

<script>
import Card from "../components/Card.vue";

export default {
  name: "CardContainer",
  components: {
    Card
  }
};
</script>

<style>
#CardContainer {
  color: #2c3e50;
  height: 87vh;
  width: 100%;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
}
</style>
