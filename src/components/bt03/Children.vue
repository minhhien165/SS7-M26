<template>
  <div>
    <h3>---------Children component-----------</h3>
    <button @click="handleIncrease">increase</button>
  </div>
</template>
<script setup>
import { ref } from "vue";
const emit = defineEmits(["emit"]);
const count = ref(0);
const handleIncrease = () => {
  count.value++;
  emit("emit", count);
};
</script>
<style></style>
