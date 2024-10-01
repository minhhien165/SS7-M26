<!-- <template>
  <div>
    <h1>session07</h1>
    <ul>
      <li>Props</li>
      <li>Slots</li>
      <li>Emit</li>
    </ul>
    <Parent></Parent>
  </div>
</template>
<script setup>
import Parent from "./components/Parent.vue";
</script>
<style scoped></style> -->

<template>
  <div>
    <Parent></Parent>
    <Parent2></Parent2>
    <Parent3></Parent3>
    <Parent4></Parent4>
    <br />
    <Modal></Modal>
    <Card></Card>
    <MessageParent></MessageParent>
    <ListUser></ListUser>
    <br />
    <BaseButton></BaseButton>
    <br />
    <BaseInput></BaseInput>
  </div>
</template>
<script setup>
import Parent from "./components/bt01/Parent.vue";
import Parent2 from "./components/bt02/Parent.vue";
import Parent3 from "./components/bt03/Parent.vue";
import Parent4 from "./components/bt04/Parent.vue";
import Modal from "./components/bt05/Modal.vue";
import Card from "./components/bt06/Card.vue";
import MessageParent from "./components/bt07/MessageParent.vue";
import ListUser from "./components/bt08/ListUser.vue";
import BaseButton from "./components/bt09/BaseButton.vue";
import BaseInput from "./components/bt10/BaseInput.vue";
</script>
<style scoped></style>
