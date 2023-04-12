<template>
  <main>
    <!-- heading -->
    <header>
      <img src="https://pinia.vuejs.org/logo.svg" alt="pinia logo" />
      <h1>Pinia Tasks</h1>
    </header>
  </main>
  <div class="is-flex is-justify-content-center is-align-content-center">
    <TaskForm />
  </div>
  <!-- tasks list -->
  <div v-for="task in taskStore.tasks" :key="task.id">
    <TaskDetails :task="task" />
  </div>
</template>

<script>
import TaskForm from "./components/TaskForm.vue";
import TaskDetails from "./components/TaskDetails.vue";
import { useTaskStore } from "@/stores/TaskStore.js";

export default {
  components: { TaskForm, TaskDetails },

  setup() {
    const taskStore = useTaskStore();
    return { taskStore };
  },
};
</script>