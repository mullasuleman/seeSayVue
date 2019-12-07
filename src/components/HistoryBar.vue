<template>
  <div id="HistoryBar">
    <HistoryItem />
  </div>
</template>

<script>
import HistoryItem from "./History-Item.vue";

export default {
  name: "HistoryBar",
  components: {
    HistoryItem
  }
};
</script>

<style>
#HistoryBar {
  padding: 0.25rem;
  width: 50%;
  height: 100%;
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
  background-color: rgb(36, 39, 43);
  border-radius: 1rem;
}
</style>
