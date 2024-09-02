<script setup>
import { ref } from 'vue';

const count = ref(0);

function increment() {
  count.value++;
}
</script>

<template>
  <!-- v-on 디렉티브의 축약어 @ -->
  <button @click="increment" class="btn">숫자 세기: {{ count }}</button>
  <!-- == v-on:click="increment" -->
</template>

<style lang="css" scoped>
.btn {
  min-width: 300px;
  background-color: #fff;
  font-weight: bold;
  color: black;
}
</style>
