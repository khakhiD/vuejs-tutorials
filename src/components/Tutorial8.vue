<!-- 계산된 속성 (computed attributes) -->
<script setup>
import { computed, ref } from 'vue';

let id = 0;

const newTodo = ref('');
const hideCompleted = ref(false);
const todos = ref([
  { id: id++, text: 'HTML 배우기', done: true },
  { id: id++, text: 'JavaScript 배우기', done: true },
  { id: id++, text: 'Vue 배우기', done: false },
]);

const filteredTodos = computed(() => {
  return hideCompleted.value ? todos.value.filter((t) => !t.done) : todos.value;
});

function addTodo() {
  todos.value.push({ id: id++, text: newTodo.value, done: false });
  newTodo.value = '';
}

function removeTodo(todo) {
  todos.value = todos.value.filter((t) => t !== todo);
}
</script>

<template>
  <button @click="hideCompleted = !hideCompleted">
    {{ hideCompleted ? 'Show All' : 'Hide Completed' }}
  </button>
  <form @submit.prevent="addTodo">
    <input v-model="newTodo" required placeholder="New Todo" />
    <button>Add Todo</button>
  </form>
  <ul>
    <li v-for="todo in filteredTodos" :key="todo.id">
      <input type="checkbox" v-model="todo.done" />
      <span :class="{ done: todo.done }">{{ todo.text }}</span>
      <button @click="removeTodo(todo)">X</button>
    </li>
  </ul>
</template>

<style>
.done {
  text-decoration: line-through;
}
</style>
