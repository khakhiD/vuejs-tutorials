<!-- 슬롯(slot) -->
<template>
  <ChildComponent><slot>slot asdf</slot>부모로부터: {{ msg }}</ChildComponent>
</template>
<script setup>
import { ref } from 'vue';
import { TutorialChild as ChildComponent } from './TutorialChild.vue';

const msg = ref('Vue는 개발자에게 정말 유용하죠!');
</script>
<style lang=""></style>
