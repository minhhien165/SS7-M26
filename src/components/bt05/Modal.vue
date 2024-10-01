<template>
  <div class="modal" v-if="isVisible">
    <div class="modal-content">
      <span class="close" @click="closeModal">&times;</span>
      <h2>Thông báo từ hệ thống</h2>
      <p>
        Đây là nội dung của modal. Bạn có thể đóng modal bằng cách nhấn vào nút
        Close
      </p>
      <button @click="closeModal">Close</button>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const isVisible = ref(true);

const closeModal = () => {
  isVisible.value = false;
};
</script>

<style scoped>
.modal {
  display: flex;
  justify-content: center;
  align-items: center;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
}

.modal-content {
  background-color: white;
  padding: 20px;
  border-radius: 5px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  width: 300px;
  text-align: center;
}

.close {
  float: right;
  font-size: 20px;
  cursor: pointer;
}
</style>
