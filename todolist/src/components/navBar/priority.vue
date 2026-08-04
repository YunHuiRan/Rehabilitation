<template>
  <h2>priority</h2>

  <div class="w-full flex flex-col gap-2 select-none">
    <div
      v-for="(priority, index) in priorityStats"
      :key="index"
      class="w-full flex items-center gap-1 hover:cursor-pointer"
    >
      <priorityFlag :level="priority.level" class="w-8" />

      <span>{{ priority.label }}</span>

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

<style></style>
