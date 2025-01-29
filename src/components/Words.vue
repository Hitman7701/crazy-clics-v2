<script setup>
import { wordsList } from '@/assets/data'

const emit = defineEmits(['correctWord'])
</script>

<template>
  <div>
    <button @click="$emit('CorrectWord', word)" v-for="word in wordsList" :key="word">
      {{ word }}
    </button>
  </div>
</template>

<style scoped>
div {
  display: flex;
  gap: 30px;
}

button {
  background-color: #5fe3b3;
  border-radius: 5px;
  padding: 15px;
  border: none;
}
</style>
