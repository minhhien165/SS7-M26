<template>
  <div>
    <h1>---------Children component--------</h1>
    <p>children company: {{ prop.data }}</p>
  </div>
</template>
<script setup>
const prop = defineProps(["data"]);
</script>
<style></style>
