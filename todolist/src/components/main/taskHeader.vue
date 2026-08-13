<template>
  <div class="flex justify-between h-10">
    <!-- title -->
    <div class="flex gap-4 justify-center select-none">
      <h1 class="text-3xl">All Tasks</h1>

      <h2 class="opacity-60 flex items-center">7 tasks</h2>
    </div>

    <div class="flex justify-center items-center gap-6">
      <!-- search bar -->
      <div id="task-search-bar">
        <searchIcon class="h-5"></searchIcon>
        <input
          type="text"
          placeholder="search task..."
          class="indent-2 focus:outline-none"
        />
      </div>

      <!-- selection bar -->
      <label id="selection-bar" class="select-none hover:cursor-pointer">
        <h2>sort :</h2>

        <select
          name="sort"
          class="h-full p-2 focus:outline-none hover:cursor-pointer"
        >
          <option>create time</option>
          <option>update time</option>
          <option>start time</option>
          <option>end time</option>
        </select>
      </label>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineAsyncComponent } from "vue";

const searchIcon = defineAsyncComponent(
  () => import("@/assets/taskHeader/searchIcon.vue"),
);
</script>

<style scoped>
#task-search-bar,
#selection-bar {
  display: flex;
  align-items: center;
  gap: 0.6rem;
  padding: 0.5rem;
  border-radius: var(--card-border-radius);
}

#task-search-bar:hover,
#selection-bar:hover {
  transition: var(--item-transition);
  box-shadow: var(--card-shadow);
  background-color: var(--primary-color-light);
}
</style>
