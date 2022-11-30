<script setup>
import { ref } from 'vue'
const items = [
  {
    id: 1,
    name: '大吉',
    description:
      '大吉です'
  },
  {
    id: 2,
    name: '中吉',
    description:
      '中吉です'
  },
  {
    id: 3,
    name: '小吉',
    description:
      '小吉です'
  },
  {
    id: 4,
    name: '吉',
    description:
      '吉です'
  },
  {
    id: 5,
    name: '凶',
    description:
      '凶です'
  }
  ]
// リアクティブな状態
const result = ref(0)

// 状態を変更し、更新をトリガーする関数。
function fortune() {
  const min = 1 ;
  result.value = Math.floor( Math.random() * (items.length) + min);
}

</script>

<template>
  <template v-for="item in items">
    <div v-if="item.id === result">
      <h1>{{ item.name }}</h1>
    </div>
  </template>

  <button @click="fortune">おみくじ</button>
</template>