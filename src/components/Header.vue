<template>
  <div class="Header">
    <h1>{{title}}</h1>
    <hr>
    <p>{{intro}}</p>
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
  padding: 0.5rem 0rem;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  width: 100vw;
  /* height: 10vh; */
  background-color: #07252e;
  font-family: "Cinzel", serif;
  color: #faa533;
}

h1 {
  text-align: center;
  letter-spacing: 1rem;
}

hr {
  height: 1px;
  width: 40%;
  background: #faa533;
  border: none;
  border-radius: 2px;
}

p {
  margin-top: 0.5rem;
  letter-spacing: 1px;
}
</style>
