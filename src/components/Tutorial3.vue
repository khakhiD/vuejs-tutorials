<script setup>
import { ref } from 'vue';

const titleClass = ref('title');
</script>

<template>
  <h1 :id="titleClass">나를 빨갛게 만들어 보세요</h1>
</template>

<style>
.title {
  color: red;
}
</style>
