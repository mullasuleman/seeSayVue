<template>
  <div id="HistoryItem">
    <h3>Item</h3>
  </div>
</template>

<script>
export default {
  name: "HistoryItem"
};
</script>

<style>
#HistoryItem {
  height: 100%;
  width: 80px;
  background-color: rgba(212, 212, 212, 0.295);
  border-radius: 1rem;
  transition: 0.2s ease-in;
}

#HistoryItem:hover {
  background-color: rgba(212, 212, 212, 0.678);
  transform: scale(1.1);
  cursor: pointer;
}
</style>
