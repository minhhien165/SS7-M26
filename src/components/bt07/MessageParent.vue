<template>
  <div>
    <MessageChildren @emit="handleEmit"></MessageChildren>
  </div>
</template>
<script setup>
import { ref } from "vue";
import MessageChildren from "./MessageChildren.vue";

const handleEmit = (data) => {
  alert(data);
};
</script>
<style></style>
