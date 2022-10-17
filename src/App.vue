<template>
  <h2>Welcome to my calculator</h2>
  <VueCal />
</template>

<script>
import VueCal from "./components/VueCalculator.vue";
export default {
  name: "App",
  components: { VueCal },
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
