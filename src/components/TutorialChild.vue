<script setup>
import { ref } from 'vue';

const props = defineProps({
  msg: String,
});

const emit = defineEmits(['response']);
emit('response', '자식 컴포넌트로부터 받은 데이터에요!');
</script>

<template>
  <h1>{{ msg }}</h1>
</template>
