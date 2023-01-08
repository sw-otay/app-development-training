<script setup>
import { ref, computed } from 'vue'
const items = ['大吉','中吉','小吉','吉','凶']
const resultVal = ref('')
const resultNum = ref(0)

function makeFortune() {
  resultNum.value = Math.floor( Math.random() * (items.length));
  resultVal.value = randomize.value;
}
const randomize = computed(() => {
  return items[resultNum.value]
})
</script>

<template>
  <p>{{ resultVal }}</p>
  <button @click="makeFortune">おみくじ</button>
</template>