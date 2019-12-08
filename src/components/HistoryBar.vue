<template>
  <div id="HistoryBar">
    <HistoryItem v-for="(item, index) in history" :key="index" :imgSrc="item" />
  </div>
</template>

<script>
import HistoryItem from "./History-Item.vue";

export default {
  name: "HistoryBar",
  components: {
    HistoryItem
  },
  props: {
    history: Array
  }
};
</script>

<style>
#HistoryBar {
  margin-bottom: 30px;
  padding: 0.5rem;
  width: 83vw;
  height: 100px;
  display: flex;
  flex-direction: row-reverse;
  justify-content: flex-end;
  align-items: center;
  background-color: rgb(36, 39, 43);
  border-radius: 1rem;
  /* border: 2px solid snow; */
}
</style>
