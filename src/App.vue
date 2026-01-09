<script setup>
  import { ref } from 'vue';
  const newTask = ref('');
</script>


<template>
  <!-- Vue.js provides several built-in directives for common tasks
  such as conditional rendering, list rendering, event handling, and attribute binding -->
  <main>
    <h1>Write Your Tasks</h1>
    <form>
      <label>
        New Task: 
        <input  v-model="newTask" name="newTask">
      </label>
      <button type="submit">Add Task</button>
    </form>
    <p>{{ newTask }}</p>
  </main>
</template>


<style scoped>
  main {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  color: #2c3e50;
  margin-top: -40px;
}
h1 {
  font-weight: normal;
}
</style>