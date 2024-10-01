<template>
  <div class="product-info">
    <headers>
      <template #header>
        <h2>Thông tin sản phẩm</h2>
      </template>
    </headers>
    <bodys>
      <template #body>
        <p>
          Đây là mô tả ngắn gọn về sản phẩm này. Sản phẩm có các tính năng nổi
          bật và giá cả hợp lý.
        </p>
      </template>
    </bodys>
    <footers>
      <template #footer>
        <button class="detail-button">Xem chi tiết</button>
      </template>
    </footers>
  </div>
</template>

<script setup>
import headers from "./header.vue";
import bodys from "./body.vue";
import footers from "./footer.vue";
</script>

<style scoped>
.product-info {
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  padding: 20px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  max-width: 400px;
  margin: 20px auto;
  text-align: center;
}

.product-info h2 {
  margin-bottom: 10px;
}

.product-info p {
  margin-bottom: 20px;
  color: #555;
}

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
