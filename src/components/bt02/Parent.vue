<template>
  <div>
    <Children :data="data"></Children>
  </div>
</template>
<script setup>
import Children from "./Children.vue";

const data = {
  id: 1,
  name: "mít",
  price: 12000,
  quantity: 10,
};
</script>
<style></style>
