<script setup lang="ts">
import { computed, ref } from 'vue';
import Tutorial1 from './Tutorial1.vue';
import Tutorial2 from './Tutorial2.vue';
import Tutorial3 from './Tutorial3.vue';
import Tutorial4 from './Tutorial4.vue';
import Tutorial5 from './Tutorial5.vue';
import Tutorial6 from './Tutorial6.vue';
import Tutorial7 from './Tutorial7.vue';
import Tutorial8 from './Tutorial8.vue';
import Tutorial9 from './Tutorial9.vue';
import Tutorial10 from './Tutorial10.vue';
import Tutorial11 from './Tutorial11.vue';
import Tutorial12 from './Tutorial12.vue';
import Tutorial13 from './Tutorial13.vue';
import Tutorial14 from './Tutorial14.vue';
import Tutorial15 from './Tutorial15.vue';

const tutorials = ref([
  { id: 1, name: '시작하기' },
  { id: 2, name: '선언적 렌더링' },
  { id: 3, name: '속성 바인딩' },
  { id: 4, name: '이벤트 리스너' },
  { id: 5, name: '폼(form) 바인딩' },
  { id: 6, name: '조건부 렌더링' },
  { id: 7, name: '리스트 렌더링' },
  { id: 8, name: '계산된 속성' },
  { id: 9, name: '생명주기와 템플릿 참조' },
  { id: 10, name: '감시자' },
  { id: 11, name: '컴포넌트' },
  { id: 12, name: 'Props' },
  { id: 13, name: 'Emits' },
  { id: 14, name: '슬롯' },
  { id: 15, name: '훌륭하게 해냈군요!' },
]);

const currentTutorial = ref<number | null>(null);
const currentComponent = computed(() => {
  switch (currentTutorial.value) {
    case 1:
      return Tutorial1;
    case 2:
      return Tutorial2;
    case 3:
      return Tutorial3;
    case 4:
      return Tutorial4;
    case 5:
      return Tutorial5;
    case 6:
      return Tutorial6;
    case 7:
      return Tutorial7;
    case 8:
      return Tutorial8;
    case 9:
      return Tutorial9;
    case 10:
      return Tutorial10;
    case 11:
      return Tutorial11;
    case 12:
      return Tutorial12;
    case 13:
      return Tutorial13;
    case 14:
      return Tutorial14;
    case 15:
      return Tutorial15;
    default:
      return null;
  }
});
</script>

<template>
  <div class="main">
    <h1>Vue3 Composition Tutorials</h1>
    <div class="header">
      <div>
        <li
          class="buttonList"
          v-for="tutorial in tutorials"
          :key="tutorial.id"
          @click="currentTutorial = tutorial.id">
          <button class="mainBtn">
            {{ tutorial.id }}. {{ tutorial.name }}
          </button>
        </li>
      </div>
      <div class="component">
        <component :is="currentComponent"></component>
      </div>
    </div>
  </div>
</template>

<style scoped>
.buttonList {
  list-style: none;
  display: flex;
  justify-content: end;
}
.main {
  display: flex;
  flex-direction: column;
}
.header {
  display: flex;
  gap: 5rem;
  padding-bottom: 1rem;
}
.component {
  width: 100%;
  margin: auto;
}
.mainBtn {
  margin-right: 5px;
  margin-bottom: 5px;
  padding: 5px 10px;
  background-color: #29885d;
  color: white;
  border: none;
  cursor: pointer;
  border-radius: 5px;
  width: max-content;
}
.mainBtn:hover {
  background-color: #3a9c76;
}
li {
  display: flex;
  margin: auto;
}
</style>
