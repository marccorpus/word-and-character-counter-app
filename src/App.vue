<template>
  <div id="app">
    <Counter />
  </div>
</template>

<script>
import Counter from "./components/Counter.vue";

export default {
  components: {
    Counter,
  },
};
</script>

<style>
body {
  background-color: #efb54a !important;
}
#app {
  font-family: "Quicksand", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin-top: 50px;
}
</style>
