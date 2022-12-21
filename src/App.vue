<script setup>
import { ref } from 'vue'
const items = ['大吉','中吉','小吉','吉','凶']
const resultVal = ref('')

function makeFortune() {
  resultVal.value = items[Math.floor( Math.random() * (items.length))];
}
</script>

<template>
  <p>{{ resultVal }}</p>
  <button @click="makeFortune">おみくじ</button>
</template>