<template>
  <div id="CardContainer">
    <Card v-for="(item, index) in cardData" :key="index" :imgSrc="item.source" :name="item.name" />
  </div>
</template>

<script>
import Card from "../components/Card.vue";

export default {
  name: "CardContainer",
  components: {
    Card
  },
  props: {
    cardData: Array
  }
};
</script>

<style>
#CardContainer {
  padding: 1rem 3rem;
  color: #2c3e50;
  min-height: 100%;
  height: 82vh;
  width: 75%;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: flex-start;
}
</style>
