<template>
  <div>
    <h1>Child</h1>
    <slot name="slot1" :item="data"></slot>
    <button @click="handleClick">Send message</button>
  </div>
</template>
<script setup>
const props = defineProps(["propName", "message2", "mess3"]);
const emit = defineEmits(["messageEmit"]);

const handleClick = () => {
  emit("messageEmit", "Hello no problem");
};

console.log("giá trị Prop", props.propName);
console.log("giá trị mess2", props);
</script>
<style></style>
