<script setup>
import { ref } from 'vue';

const titleClass = ref('title');
</script>

<template>
  <h2 :class="titleClass">나를 빨갛게 만들어 보세요</h2>
</template>

<style>
.title {
  color: red;
}
</style>
