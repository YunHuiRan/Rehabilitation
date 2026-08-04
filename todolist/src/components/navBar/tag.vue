<template>
  <div>
    <h2 class="select-none mb-2 p-2">tags</h2>

    <div
      v-for="(tag, index) in tagStats"
      :key="index"
      class="priority-container"
    >
      <div class="flex gap-2">
        <tagIcon :color="tag.color" class="w-6"></tagIcon>

        <span>{{ tag.tagName }}</span>
      </div>

      <span>{{ tag.taskCount }}</span>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineAsyncComponent } from "vue";

const tagIcon = defineAsyncComponent(() => import("@/assets/tag/tagIcon.vue"));

type tagInfo = {
  color: string;
  tagName: string;
  taskCount: number;
};

const tagStats: tagInfo[] = [
  { color: "#6EB6FA", tagName: "study", taskCount: 5 },
  { color: "#9A6AE9", tagName: "work", taskCount: 10 },
  { color: "#5DC9AC", tagName: "personal", taskCount: 15 },
  { color: "#C4C8CB", tagName: "other", taskCount: 15 },
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
