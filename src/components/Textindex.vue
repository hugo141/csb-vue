
<template>
  <div>
    <Textlbl text="件名" classdef="left" />
    <select
      style="width: 99%; font-size: 16px"
      v-model="selected"
      v-on:change="selectItem"
    >
      <option v-for="item in items" :key="item.id" v-bind:value="item.id">
        {{ item.title }}
      </option>
    </select>
    <span>{{ selected }}</span>
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
  data() {
    return { selected: 0 };
  },
  methods: {
    selectItem: function (e) {
      this.$emit("select-key", e.target.value);
    },
  },
};
</script>