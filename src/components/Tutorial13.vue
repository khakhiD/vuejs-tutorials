<!-- Emits -->
<script setup>
import { ref } from 'vue';
import ChildEmits from './ChildEmits.vue';

const childMsg = ref('자식 컴포넌트로부터 아직 메시지를 받지 못했어요!');
</script>

<template>
  <ChildEmits @response="(msg) => (childMsg = msg)" />
  <p>{{ childMsg }}</p>
</template>

<style scoped>
p {
  width: full;
  text-align: center;
  border: 1px solid gray;
  padding-top: 2rem;
  padding-bottom: 2rem;
}
</style>
