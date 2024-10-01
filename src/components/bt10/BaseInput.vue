<template>
  <div class="input-container">
    <slot name="prepend"></slot>
    <input
      :type="type"
      :placeholder="placeholder"
      :value="modelValue"
      @input="handleInput"
    />
    <slot name="append"></slot>
  </div>
</template>

<script setup>
const props = defineProps({
  placeholder: {
    type: String,
    default: "",
  },
  type: {
    type: String,
    default: "text",
  },
  modelValue: {
    type: String,
    default: "",
  },
});

const emit = defineEmits(["update:modelValue"]);

const handleInput = (event) => {
  emit("update:modelValue", event.target.value);
};
</script>

<style scoped>
.input-container {
  display: flex;
  align-items: center;
}

input {
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
  flex: 1;
  margin: 0 5px;
}

input:focus {
  border-color: #007bff;
}
</style>
