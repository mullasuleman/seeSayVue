<template>
  <div class="Header">
    <h1>{{title}}</h1>
    <hr>
    <pre>{{intro}}</pre>
  </div>
</template>

<script>
	export default {
    name: "Header",
    props: {
      title: String,
      intro: String
    }
	};
</script>

<style scoped>
.Header {
  padding: 1rem 0rem;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  width: 100vw;
  /* height: 10vh; */
  background-color: #07252e;
  font-family: "Cinzel", serif;
  color: #faa533;
  text-align: center;
}

h1 {
  text-transform: uppercase;
  letter-spacing: 1rem;
  padding: 1rem;
}

hr {
  height: 3px;
  width: 10%;
  margin-left: -1rem;
  background: #faa533;
  border: 0.5px solid #faa533;
  border-radius: 5px;
}

pre {
  margin-top: 1rem;
  letter-spacing: 1.5px;
  width: 50%;
  font-family: "Cinzel", serif;
}
</style>
