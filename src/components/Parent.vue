<template>
  <div>
    <h1>Parent</h1>
    <Child
      :propName="message"
      :message2="message2"
      :mess3="mess3"
      @messageEmit="handleEmit"
    >
      <template #slot1>
        <h3>Slots</h3>
        <p>Item child: {{ item }}</p>
        <button @click="handleClick">click</button>
      </template>

      <template #slot2>
        <h3>Slots1111</h3>
      </template>
    </Child>
  </div>
</template>
<script setup>
import Child from "./Child.vue";

let message = "hello";
let message2 = "Hi";
let mess3 = "111";

const handleClick = () => {
  console.log("get acess");
};

const handleEmit = (data) => {
  console.log(data);
};
</script>
<style></style>
