<template>
  <div class="flex gap-1">
    <button
      v-for="(tab, index) in tabs"
      :key="index"
      :id="selectedTab === tab.value ? 'selected-tab' : ''"
      class="breadcrumb-button"
      @click="selectedTab = tab.value"
    >
      {{ tab.label }}
    </button>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
const tabs = [
  { label: "All", value: "all" },
  { label: "Pending", value: "pending" },
  { label: "Active", value: "active" },
  { label: "Completed", value: "completed" },
];

const selectedTab = ref("all");
</script>

<style scoped>
.breadcrumb-button {
  background-color: white;
  color: black;
  width: 100px;
  padding-top: 0.5rem;
  padding-bottom: 0.5rem;
  border-radius: 5px;
  transition: var(--item-transition);
}

.breadcrumb-button:hover {
  cursor: pointer;
  background-color: var(--primary-color-light);
}

#selected-tab {
  background-color: var(--primary-color);
  color: white;
}
</style>
