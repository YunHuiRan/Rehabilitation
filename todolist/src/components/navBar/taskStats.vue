<template>
  <div class="w-full">
    <div v-for="task in taskStats" :key="task.name" class="base-task">
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
  () => import("@/assets/taskIcons/allTask.vue"),
);
const pendingTask = defineAsyncComponent(
  () => import("@/assets/taskIcons/pendingTask.vue"),
);
const inProgressTask = defineAsyncComponent(
  () => import("@/assets/taskIcons/InProgressTask.vue"),
);
const completedTask = defineAsyncComponent(
  () => import("@/assets/taskIcons/completedTask.vue"),
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
.base-task {
  width: 100%;
  padding: 0.5rem;
  margin-bottom: 0.7rem;
  display: flex;
  background-color: var(--primary-color-light);
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  border-radius: 0.5rem;
}

.base-task:hover {
  cursor: pointer;
}
</style>
