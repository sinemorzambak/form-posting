<template>
  <div id="app">
    <h1>Başvuru Formu</h1>
    <PostComponent />

  </div>
</template>

<script>

import PostComponent from "./components/PostComponent";

// <style scoped src="@/src/assets/main.css">
// </style>

export default {
  name: "App",
  components: {
    PostComponent,
  }
};
</script>

<style>
  /* @import './assets/main.css'; */

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px; }

</style>
