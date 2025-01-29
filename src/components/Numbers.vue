<script setup>
import { numbersList } from '@/assets/data'
</script>

<template>
  <div>
    <button v-for="number in numbersList" :key="index">{{ number }} km</button>
  </div>
</template>

<style scoped>
div {
  display: flex;
  gap: 40px;
}

button {
  background-color: #b768e0;
  border-radius: 5px;
  padding: 15px;
  border: none;
}
</style>
