<template>
  <div>
    <h1>----------List User------------</h1>
    <button class="detail-button" @click="handleShow">Add user</button>
    <FormAddUser v-show="form" @emitForm="handleForm"></FormAddUser>
  </div>
</template>
<script setup>
import { ref } from "vue";
import FormAddUser from "./FormAddUser.vue";
let form = ref(false);
const handleForm = (data) => {
  console.log(data.value);

  form.value = data.value;
};
const handleShow = () => {
  form.value = true;
};
</script>
<style scoped>
.detail-button {
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 5px;
  padding: 10px 20px;
  cursor: pointer;
  font-size: 16px;
}

.detail-button:hover {
  background-color: #0056b3;
}
</style>
