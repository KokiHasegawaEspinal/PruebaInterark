<script setup>
import { ref } from 'vue'

// dar a cada tarea (todo) un id único
let id = 0

const newTodo = ref('')
const todos = ref([
  { id: id++, text: 'レッスン１' },
  { id: id++, text: 'レッスン２' },
  { id: id++, text: 'レッスン３' },
  { id: id++, text: 'レッスン４' }
])

function addTodo() {
  todos.value.push({ id: id++, text: newTodo.value })
  newTodo.value = ''
}

function removeTodo(todo) {
  todos.value = todos.value.filter((t) => t !== todo)
}
</script>

<template>
  <form @submit.prevent="addTodo">
    <input v-model="newTodo">
    <button>Enter your Task</button>
  </form>
  <ul>
    <li v-for="todo in todos" :key="todo.id">
      {{ todo.text }}
      <button @click="removeTodo(todo)">X</button>
    </li>
  </ul>
</template>