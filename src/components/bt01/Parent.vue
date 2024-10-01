<template>
  <div>
    <h1>---------Parent component--------</h1>
    <p>parent company: {{ data }}</p>
    <Children :data="data"></Children>
  </div>
</template>
<script setup>
import Children from "./Children.vue";

const data = "Rikkei Academy";
</script>
<style></style>
