<template>
    <div>
      <button @click="activeBtn(x - 1)" v-for="x in 3" :key="x" :class="{ active: activeIndex === x - 1 }">
        button {{ x }}
      </button>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  let activeIndex = ref(0);
  const activeBtn = (count) => {
    activeIndex.value = count;
  };
  </script>
  
  <style>
  .active {
    background-color: red;
    color: #fff;
  }
  </style>