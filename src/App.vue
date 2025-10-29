<template>
  <div class="container">
    <h1>Список дел</h1>
    <TaskItem
      v-for="task in tasks"
      :key="task.id"
      :task="task"
    />
  </div>
</template>

<script setup lang="ts">
import TaskItem from './components/TaskItem.vue'

interface Task {
  id: number
  title: string
  text: string
}

const tasks: Task[] = [
  { id: 1, title: 'Магазин', text: 'Купить продуктов: молоко+хлеб' },
  { id: 2, title: 'Колледж', text: 'Подготовить приложение VUE, написать английский ' },
  { id: 3, title: 'Дом', text: 'Убраться в комнате, помыть посуду' }
]
</script>

<style scoped>
.container {
  max-width: 600px;
  margin: 40px auto;
  padding: 20px;
  font-family: Arial, sans-serif;
}
h1 {
  text-align: center;
  color: #ffffff;
}
</style>