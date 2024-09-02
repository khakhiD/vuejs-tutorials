<template>
  <h1>{{ message }}</h1>
  <p>Counter: {{ counter.count }}</p>
</template>
<script setup>
import { reactive, ref } from 'vue';

const message = ref('Hi Vue!');
const count = reactive({
  count: 0,
});
</script>
