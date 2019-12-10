<template>
  <div id="CardContainer">
    <Card
      v-for="(item, index) in cardData"
      :key="index"
      :imgSrc="item.source"
      :name="item.name"
      :history="history"
      :audio="item.audio"
      :desc="item.desc"
    />
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
    cardData: Array,
    history: Array
  }
};
</script>

<style>
#CardContainer {
  padding: 1rem 3rem;
  color: #2c3e50;
  max-height: 92%;
  min-height: 82vh;
  width: 90vw;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: flex-start;
}
</style>
