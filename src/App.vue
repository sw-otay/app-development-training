<script setup>
import { ref, computed } from 'vue'
const items = ['大吉','中吉','小吉','吉','凶']
const resultNum = ref(0)

function makeFortune() {
  resultNum.value = Math.floor( Math.random() * (items.length));
}
const selectedFortune = computed(() => {
  return items[resultNum.value]
})
</script>

<template>
  <p>{{ selectedFortune }}</p>
  <button @click="makeFortune">おみくじ</button>
</template>