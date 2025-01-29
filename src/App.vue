<script setup>
import { ref } from 'vue'

const result = ref('')

import Colors from './components/Colors.vue'
import Numbers from './components/Numbers.vue'
import Words from './components/Words.vue'

const correctWord = (word) => {
  const firstLetter = word[0].toUpperCase()
  const otherLetters = word.slice(1).toLowerCase()

  result.value = firstLetter + otherLetters
}
</script>

<template>
  <h1>Crazy Clics V2</h1>
  <main>
    <div class="leftColumn">
      <Words @correctWord="correctWord" />
      <Colors />
      <Numbers />
    </div>
    <div class="rightColumn">
      <div>
        <p>👇 Le résultat 👇</p>
        <div class="resultat">{{ result }}</div>
      </div>
    </div>
  </main>
</template>

<style scoped>
h1 {
  margin-top: 50px;
  font-size: 45px;
  font-weight: bold;
  margin-bottom: 50px;
  text-align: center;
}

main {
  display: flex;
  height: 100vh;
  width: 100vw;
  margin: 0 auto;
  border: 1px green solid;
}

.leftColumn {
  display: flex;
  flex-direction: column;
  border: 1px red solid;
  flex: 2;
  gap: 150px;
  justify-content: center;
  align-items: center;
}

.rightColumn {
  display: flex;
  justify-content: center;
  align-items: center;
  border: 1px blue solid;
  flex: 1;
}
p {
  font-weight: bold;
  margin-bottom: 20px;
  text-align: center;
}

.resultat {
  width: 250px;
  height: 50px;
  border: double 3px black;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
