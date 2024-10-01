<template>
  <div>
    <h3>---------Parent Component-----------</h3>
    <p>Count: {{ count.value }}</p>
    <Child @emit="handleEmit"></Child>
  </div>
</template>
<script setup>
import { ref } from "vue";
import Child from "./Children.vue";

const count = ref(0);

const handleEmit = (data) => {
  const dataChildren = ref(data.value);
  count.value = dataChildren;
};
</script>
<style></style>
