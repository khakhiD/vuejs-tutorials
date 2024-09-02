<!-- 슬롯(slot) -->
<script setup>
import { ref } from 'vue';
import ChildSlot from './ChildSlot.vue';

const msg = ref('Vue는 개발자에게 정말 유용하죠!');
</script>

<template>
  <ChildSlot>부모로부터: {{ msg }}</ChildSlot>
</template>
