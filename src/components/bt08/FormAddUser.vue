<template>
  <div class="form-container">
    <h2>Form Add User</h2>
    <form @submit.prevent="submitForm">
      <div class="form-group">
        <label for="name">Name</label>
        <input type="text" id="name" v-model="name" required />
      </div>
      <div class="form-group">
        <label for="email">Email</label>
        <input type="email" id="email" v-model="email" required />
      </div>
      <div class="form-group">
        <label for="address">Address</label>
        <input type="text" id="address" v-model="address" required />
      </div>
      <button type="button" class="close-button" @click="closeForm">
        Close
      </button>
      <button type="submit" class="submit-button">Submit</button>
    </form>
  </div>
</template>

<script setup>
import { ref } from "vue";

const name = ref("");
const email = ref("");
const address = ref("");

const submitForm = () => {
  console.log("Form submitted:", {
    name: name.value,
    email: email.value,
    address: address.value,
  });
};

const emit = defineEmits(["emitForm"]);
let form = ref(false);

const closeForm = () => {
  form.value = false;
  emit("emitForm", form);
  name.value = "";
  email.value = "";
  address.value = "";
};
</script>

<style scoped>
.form-container {
  background-color: white;
  border-radius: 8px;
  padding: 20px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  max-width: 400px;
  margin: 20px auto;
  border: 1px solid #e0e0e0;
}

h2 {
  text-align: center;
  margin-bottom: 20px;
}

.form-group {
  margin-bottom: 15px;
}

label {
  display: block;
  margin-bottom: 5px;
}

input {
  width: 100%;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

.close-button {
  background-color: #f44336;
  color: white;
  border: none;
  border-radius: 5px;
  padding: 10px 15px;
  cursor: pointer;
  margin-right: 10px;
}

.submit-button {
  background-color: #4caf50;
  color: white;
  border: none;
  border-radius: 5px;
  padding: 10px 15px;
  cursor: pointer;
}

.close-button:hover,
.submit-button:hover {
  opacity: 0.9;
}
</style>
