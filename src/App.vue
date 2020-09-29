<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Star rating component demo" />
    <StarRating ratio="1" />
    <StarRating ratio="2" />
    <StarRating ratio="3" />
    <StarRating ratio="4" />
    <StarRating ratio="5" />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import StarRating from "./components/StarRating.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    StarRating,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
