<script setup>
import { ref } from 'vue';

const text = ref('');

// function onInput(e) {
//   text.value = e.target.value
// }
</script>

<template>
  <!-- v-model 디렉티브가 양방향 데이터 바인딩을 가능하게 하므로, 이벤트 핸들러를 사용할 필요가 없어진다. -->
  <input v-model="text" placeholder="여기에 입력하기" />
  <p>{{ text }}</p>
</template>
