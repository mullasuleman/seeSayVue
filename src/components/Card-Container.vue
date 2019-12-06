<template>
  <div id="CardContainer">
    <!-- Cards are just here temporarily for testing -->
    <Card />
    <Card />
    <Card />
    <Card />
    <Card />
    <Card />
    <Card />
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
  padding: 1rem 3rem;
  color: #2c3e50;
  min-height: 100%;
  height: 82vh;
  width: 80%;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: flex-start;
}
</style>
