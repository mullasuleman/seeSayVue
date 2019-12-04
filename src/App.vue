<template>
  <div id="App">
    <Header />
    <CardContainer />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer";
import CardContainer from "./components/Card-Container.vue";

export default {
  name: "app",
  components: {
    Header,
    CardContainer,
    Footer
  }
};
</script>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

#App {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  color: #2c3e50;
  max-height: 100vh;
  width: 100vw;
}
</style>
