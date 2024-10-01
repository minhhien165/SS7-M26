<template>
  <div>
    <h3>-----------TodoItem component-----------</h3>
    <button @click="handleClick">Delete</button>
  </div>
</template>
<script setup>
const emit = defineEmits(["emit"]);
const item = {
  id: 1,
  name: "item1",
};
const handleClick = () => {
  emit("emit", item);
};
</script>
<style></style>
