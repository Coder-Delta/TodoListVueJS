<script setup>
import TaskForm from './components/TaskForm.vue';

function addTask(task) {
  console.log('Received in parent:', task);
}
</script>

<template>
  <main>
    <TaskForm @addTask="addTask" />
  </main>
</template>
