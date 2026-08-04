<template>
  <div class="flex flex-col gap-4">
    <logo />

    <taskStats />
  </div>
</template>

<script setup lang="ts">
import { defineAsyncComponent } from "vue";

const logo = defineAsyncComponent(() => import("./logo.vue"));
const taskStats = defineAsyncComponent(() => import("./taskStats.vue"));
</script>

<style></style>
