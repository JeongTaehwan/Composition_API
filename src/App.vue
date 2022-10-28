<template>
  <refReactive />
  <stopWatchEffect />
</template>

<script>
import stopWatchEffect from "./components/stopWatchEffect.vue";

export default {
  name: "App",
  components: {
    stopWatchEffect,
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
