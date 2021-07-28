<template>
  <div>
    <select>
      <option v-for="item in items" :key="item.id">
        {{ item.id }}
      </option>
    </select>
  </div>
</template>

<script>
export default {
  name: "Textindex",
  props: {
    items: String,
  },
};
</script>