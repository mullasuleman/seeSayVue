<template>
  <div id="HistoryBar">
    <HistoryItem v-for="(item, index) in history" :key="index" :imgSrc="item.source" :audioSrc="item.audio" />
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
  background-color: #07252e;
  border-radius: 1rem;
  box-shadow: 0px 0px 14px 1px rgba(222, 222, 222, 0.2);
}
</style>