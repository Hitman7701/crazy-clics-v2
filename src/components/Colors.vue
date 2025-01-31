<script setup>
const emit = defineEmits(['randomColor'])
</script>

<template>
  <div>
    <button @click="$emit('randomColor')">Couleur surprise</button>
  </div>
</template>

<style scoped>
button {
  color: #57c6df;
  border: #57c6df 2px solid;
  border-radius: 60px;
  font-size: 20px;
  padding: 20px;
  background-color: white;
}
</style>
