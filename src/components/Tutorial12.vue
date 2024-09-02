<!-- Props -->
<script setup>
import { ref } from 'vue';
import ChildProps from './ChildProps.vue';

const greeting = ref('부모 컴포넌트로부터 prop을 전달받았어요!');
</script>

<template>
  <ChildProps :msg="greeting" />
</template>
