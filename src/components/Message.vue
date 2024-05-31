<template>
    <p class="message">{{ message }}</p>
  </template>
  
  <script setup>
  defineProps({
    message: String
  });
  </script>
  
  <style scoped>
  </style>
  