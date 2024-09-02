<template>
  <h2>{{ message }}</h2>
  <p>Counter: {{ counter.count }}</p>
</template>
<script setup>
import { reactive, ref } from 'vue';

const message = ref('Hi Vue!');
const counter = reactive({
  count: 0,
});
</script>
