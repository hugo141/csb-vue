<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" width="25%" />
    <Textlbl text="件名" classdef="left" />
    <Textindex items="textdata" />
    <Textlbl text="本文" classdef="left" />
    <Textarea />
  </div>
</template>

<script>
import Textarea from "./components/Textbox";
import Textlbl from "./components/Textlbl";
import Textindex from "./components/Textindex";

export default {
  name: "App",
  components: {
    Textarea,
    Textlbl,
    Textindex,
  },
  data() {
    textdata: [
      { id: 1, title: "あ" },
      { id: 2, title: "い" },
    ];
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
