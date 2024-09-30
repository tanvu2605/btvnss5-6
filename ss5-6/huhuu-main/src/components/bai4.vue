<template>
    <div>
      <button @click="clickShow">Hiển thị</button>
      <button @click="clickHide">Ẩn</button>
      <p v-show="isVisible">Welcom to Rikkei Education</p>
    </div>
  </template>
  <script setup>
  import { ref } from "vue";
  
  const isVisible = ref(false);
  const clickShow = () => {
    isVisible.value = true;
  };
  const clickHide = () => {
    isVisible.value = false;
  };
  </script>
  <style></style>