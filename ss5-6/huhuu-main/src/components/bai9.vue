<template>
    <div>
      <h3>Gender: {{ gender }}</h3>
      <button @click="randomizeGender">Random gender</button>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const genders = ["Nam", "Nữ", "Khác"];
  
  const gender = ref("Nam");
  
  const randomizeGender = () => {
    const randomIndex = Math.floor(Math.random() * genders.length);
    gender.value = genders[randomIndex];
  };
  </script>
  
  </style>
  