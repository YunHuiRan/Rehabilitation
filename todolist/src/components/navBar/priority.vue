<template>
  <div>
    <h2 class="select-none mb-2 p-2">priority</h2>

    <div
      v-for="(priority, index) in priorityStats"
      :key="index"
      class="priority-container"
    >
      <div class="flex gap-2">
        <priorityFlag :level="priority.level" class="w-6" />

        <span>{{ priority.label }}</span>
      </div>

      <span>{{ priority.taskCount }}</span>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineAsyncComponent } from "vue";

const priorityFlag = defineAsyncComponent(
  () => import("@/assets/priority/priorityFlag.vue"),
);

type priorityInfo = {
  level: "high" | "medium" | "low";
  label: "high priority" | "medium priority" | "low priority";
  taskCount: number;
};

const priorityStats: priorityInfo[] = [
  { level: "high", label: "high priority", taskCount: 5 },
  { level: "medium", label: "medium priority", taskCount: 10 },
  { level: "low", label: "low priority", taskCount: 15 },
];
</script>

<style scoped>
.priority-container {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0.5rem;
  margin-bottom: 0.2rem;
  border-radius: var(--item-border-radius);
  transition: var(--item-transition);
  user-select: none;
}

.priority-container:hover {
  box-shadow: var(--card-shadow);
  background-color: var(--primary-color-light);
  cursor: pointer;
}
</style>
