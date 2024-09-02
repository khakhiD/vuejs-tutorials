<script setup>
import { ref } from 'vue';

const count = ref(0);

function increment() {
  count.value++;
}
</script>

<template>
  <!-- v-on 디렉티브의 축약어 @ -->
  <button @click="increment">숫자 세기: {{ count }}</button>
  <!-- == v-on:click="increment" -->
</template>
