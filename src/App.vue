<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" width="25%" />
    <Textindex
      v-bind:items="textdata"
      :selected="selectedkey"
      v-on:select-key="selectedkey = $event"
    />
    <p>{{ selectedkey }}</p>
    <p>{{ selectedtxt }}</p>
    <Textbox />
  </div>
</template>

<script>
import Textindex from "./components/Textindex.vue";
import Textbox from "./components/Textbox.vue";

export default {
  name: "App",
  components: {
    Textindex,
    Textbox,
  },
  data() {
    return {
      textdata: [
        { id: 1, title: "あ", txt: "aaaaa" },
        { id: 2, title: "い", txt: "iiiii" },
      ],
      selectedkey: 0,
      selectedtxt: null,
    };
  },
  watch: {
    selectText: function (selectedkey) {
      console.log(this.textdata[selectedkey].txt);
      this.selectedtxt = this.textdata[selectedkey].txt;
    },
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
