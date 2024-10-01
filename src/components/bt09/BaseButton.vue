<template>
  <div class="btn">
    <button type="submit" @click="handleSubmit">Submit</button>
    <button type="button" @click="handleClick">Cancel</button>
    <button type="reset" @click="handleReset">Reset</button>
  </div>
</template>

<script setup></script>

<style scoped>
.btn {
  display: flex;
  gap: 10px;
}

button {
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-size: 16px;
  background-color: #007bff;
  color: white;
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: #0056b3;
}
</style>
