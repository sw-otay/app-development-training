<script setup>
import { ref } from 'vue'
const items = ['大吉','中吉','小吉','吉','凶']
const resultNum = ref(0)
const resultVal = ref('')

function fortune() {
  const min = 0 ;
  resultNum.value = Math.floor( Math.random() * (items.length) + min);
  resultVal.value = items[resultNum.value];
}
</script>

<template>
  <h1>{{ resultVal }}</h1>
  <button @click="fortune">おみくじ</button>
</template>