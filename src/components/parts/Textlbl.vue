<template>
  <div :class="aligndef">
    <label>{{ text }}</label>
  </div>
</template>

<script>
export default {
  name: "Textlbl",
  props: {
    text: String,
    classdef: String,
  },
  computed: {
    aligndef() {
      const classdef = this.classdef;

      if (classdef === "center") {
        return "center";
      } else if (classdef === "right") {
        return "right";
      } else if (classdef === "left") {
        return "left";
      } else {
        return "center";
      }
    },
  },
};
</script>
<style scoped>
.center {
  text-align: center;
}
.right {
  text-align: right;
}
.left {
  text-align: left;
}
</style>