<template>
  <div id="textboxarea">
    <Textlbl text="本文" classdef="left" />
    <!-- <p>{{ textvalue }}</p> -->
    <textarea
      id="editer"
      name="editer"
      rows="100"
      style="width: 99%; font-size: 16px"
      v-model="textvalue"
    >
    </textarea>
  </div>
</template>

<script>
import Textlbl from "./parts/Textlbl";

export default {
  name: "Textbox",
  components: {
    Textlbl,
  },
  props: {
    txtval: String,
  },
  data() {
    return { textvalue: this.txtval };
  },
  watch: {
    txtval: function (newtextval) {
      this.textvalue = newtextval;
    },
  },
};
</script>
