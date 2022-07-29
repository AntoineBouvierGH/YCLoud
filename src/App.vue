<template>
  <FilesView></FilesView>
</template>

<script>
import FilesView from "./views/FilesView.vue";

export default {
  name: "App",
  components: {
    FilesView,
  },
};
</script>

<style>
*,
*:before,
*:after {
  box-sizing: border-box;
}

html,
body {
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  margin: 0;
  padding: 0;
  background-color: green;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width: 100%;
  height: 100%;
  background-color: red;
}
</style>
