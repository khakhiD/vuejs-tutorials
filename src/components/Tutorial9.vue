<!-- 생명주기와 템플릿 참조 -->
<script setup>
import { onMounted, ref } from 'vue';

const pElementRef = ref(null);

onMounted(() => {
  pElementRef.value.textContent = '마운트 되었어요!';
});
</script>

<template>
  <p ref="pElementRef">안녕</p>
</template>
