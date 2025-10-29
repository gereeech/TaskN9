<template>
  <div class="task-card">
    <h3>{{ task.title }}</h3>
    <p>{{ task.text }}</p>
  </div>
</template>

<script setup lang="ts">
const props = defineProps<{
  task: {
    id: number
    title: string
    text: string
  }
}>()
</script>

<style scoped>
.task-card {
  background: #f9f9f9;
  border: 1px solid #ddd;
  border-radius: 8px;
  padding: 16px;
  margin-bottom: 16px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

h3 {
  margin: 0 0 8px 0;
  color: #2c3e50;
  font-size: 1.2em;
}

p {
  margin: 0;
  color: #555;
  font-size: 0.95em;
}
</style>