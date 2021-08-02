<template>
  <div>
    <Textlbl text="件名" classdef="left" />
    <select id="titlelbl" style="width: 99%; font-size: 16px">
      <option v-for="item in items" :key="item.id">
        {{ item.title }}
      </option>
    </select>

    <Textlbl text="本文" classdef="left" />
    <textarea
      id="editer"
      name="editer"
      rows="100"
      style="width: 99%; font-size: 16px"
    >
    </textarea>
  </div>
</template>

<script>
import Textlbl from "./parts/Textlbl";

export default {
  name: "Textindex",
  components: {
    Textlbl,
  },
  props: {
    items: Array,
  },
};
</script>