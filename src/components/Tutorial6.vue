<script setup>
import { ref } from 'vue';

const bool = ref(true);

function toggle() {
  bool.value = !bool.value;
}
</script>

<template>
  <button @click="toggle">토글 버튼</button>
  <h1 v-if="bool">Vue는 굉장해! 엄청나!</h1>
  <h1 v-else>오 안돼 😢</h1>
</template>
