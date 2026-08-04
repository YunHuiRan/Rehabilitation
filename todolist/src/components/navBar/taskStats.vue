<template>
  <div>
    <div v-for="task in taskStats" :key="task.name" class="task-container">
      <div class="flex gap-2">
        <component :is="task.component"></component>

        <span>{{ task.name }}</span>
      </div>

      <span>{{ task.taskCount }}</span>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineAsyncComponent } from "vue";

const allTask = defineAsyncComponent(
  () => import("@/assets/taskIcons/allTaskIcon.vue"),
);
const pendingTask = defineAsyncComponent(
  () => import("@/assets/taskIcons/pendingTaskIcon.vue"),
);
const inProgressTask = defineAsyncComponent(
  () => import("@/assets/taskIcons/InProgressTaskIcon.vue"),
);
const completedTask = defineAsyncComponent(
  () => import("@/assets/taskIcons/completedTaskIcon.vue"),
);

type taskInfos = {
  component: any;
  name: string;
  taskCount: number;
};

const taskStats: taskInfos[] = [
  {
    component: allTask,
    name: "All",
    taskCount: 0,
  },
  {
    component: pendingTask,
    name: "Pending",
    taskCount: 0,
  },
  {
    component: inProgressTask,
    name: "In Progress",
    taskCount: 0,
  },
  {
    component: completedTask,
    name: "Completed",
    taskCount: 0,
  },
];
</script>

<style scoped>
.task-container {
  width: 100%;
  padding: 0.5rem;
  display: flex;
  gap: 0.7rem;
  margin-bottom: 0.2rem;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  border-radius: var(--item-border-radius);
  transition: var(--item-transition);
  user-select: none;
}

.task-container:hover {
  box-shadow: var(--card-shadow);
  background-color: var(--primary-color-light);
  cursor: pointer;
}
</style>
