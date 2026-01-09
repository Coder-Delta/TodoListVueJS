<script setup>
import { ref } from 'vue';

const newTask = ref('');

const emit = defineEmits(['addTask']);

function addTask() {
  emit('addTask', newTask.value);
  newTask.value = '';
}
</script>

<template>
    <main>
        <h1>Write Your Tasks</h1>
        <form @submit.prevent="addTask">
            <label>
                New Task:
                <input v-model="newTask" name="newTask">
            </label>
            <div>
                <button type="submit">Add Task</button>
            </div>
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
