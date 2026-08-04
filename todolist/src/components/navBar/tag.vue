<template>
  <div>
    <h2 class="select-none mb-2 p-2">tags</h2>

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

<script setup lang="ts"></script>

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
