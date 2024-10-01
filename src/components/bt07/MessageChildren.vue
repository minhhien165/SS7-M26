<template>
  <div>
    <button @click="handleMessage">Send message</button>
  </div>
</template>
<script setup>
const emit = defineEmits(["emit"]);
const handleMessage = () => {
  emit("emit", "Welcome to Rikkei education");
};
</script>
<style></style>
