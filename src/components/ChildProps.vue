<script setup>
import { ref } from 'vue';

const props = defineProps({
  msg: String,
});
</script>

<template>
  <p v-if="props">{{ msg }}</p>
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
