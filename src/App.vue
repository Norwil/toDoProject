<template>
  <div id="app">
    <h1>To-Do List</h1>
    <div>
      <input type="text" placeholder="Add a new task..." v-model="newTask" @keyup.enter="addTask">
      <button @click="addTask">Add Task</button>
    </div>
    <ul>
      <li v-for="task in tasks" :key="task.id">
        <input type="checkbox" v-model="task.completed">
        <span :class="{ completed: task.completed }">{{ task.text }}</span>
        <button @click="removeTask(task.id)">Remove</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      newTask: '',
      tasks: []
    };
  },
  methods: {
    addTask() {
      if (this.newTask.trim()) {
        this.tasks.push({
          id: Date.now(),
          text: this.newTask,
          completed: false
        });
        this.newTask = '';
      }
    },
    removeTask(taskId) {
      this.tasks = this.tasks.filter(task => task.id !== taskId);
    }
  }
};
</script>

