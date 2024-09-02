<!-- Props -->
<script setup>
import { ref } from 'vue';
import { TutorialChild as ChildComponent } from './TutorialChild.vue';

const greeting = ref('부모 컴포넌트로부터 prop을 전달받았어요!');
</script>

<template>
  <ChildComponent :msg="greeting" />
</template>
