<template>
  <div>
    <h1>Vue 3 Composition API Tutorials</h1>

    <div>
      <button
        v-for="tutorial in tutorials"
        :key="tutorial.id"
        @click="currentTutorial = tutorial.id">
        {{ tutorial.name }}
      </button>
    </div>

    <div>
      <!-- 현재 선택된 튜토리얼 컴포넌트 렌더링 -->
      <component :is="currentComponent"></component>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import Tutorial1 from './components/Tutorial1.vue';
import Tutorial2 from './components/Tutorial2.vue';

export default defineComponent({
  setup() {
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

    // 현재 선택된 컴포넌트를 반환
    const currentComponent = () => {
      switch (currentTutorial.value) {
        case 1:
          return Tutorial1;
        case 2:
          return Tutorial2;
        case 3:
          return Tutorial3;
        default:
          return null;
      }
    };

    return {
      tutorials,
      currentTutorial,
      currentComponent,
    };
  },
});
</script>

<style scoped>
button {
  margin-right: 10px;
  margin-bottom: 10px;
  padding: 10px 20px;
  background-color: #42b983;
  color: white;
  border: none;
  cursor: pointer;
  border-radius: 5px;
}
button:hover {
  background-color: #3a9c76;
}
</style>
