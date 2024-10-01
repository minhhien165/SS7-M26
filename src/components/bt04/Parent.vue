<template>
  <div>
    <h3>-----------TodoApp component-----------</h3>
    <p>Id to delete: {{ item.id }}</p>
    <Children @emit="handleEmit"></Children>
  </div>
</template>
<script setup>
import { ref } from "vue";
import Children from "./Children.vue";

let item = ref({});

const handleEmit = (data) => {
  item.value = data;
};
</script>
<style></style>
