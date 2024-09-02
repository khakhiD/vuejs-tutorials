<script setup>
import JSConfetti from 'js-confetti';

const confetti = new JSConfetti();

function showConfetti() {
  confetti.addConfetti();
}

showConfetti();
</script>

<template>
  <h2 @click="showConfetti">🎉 축하합니다!</h2>
</template>

<style>
h2 {
  text-align: center;
  cursor: pointer;
  margin-top: 3em;
}
</style>
