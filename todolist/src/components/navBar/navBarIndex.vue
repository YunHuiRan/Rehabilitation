<template>
  <div class="flex flex-col gap-6">
    <logo />

    <taskStats />

    <priority />

    <tag />
  </div>
</template>

<script setup lang="ts">
import { defineAsyncComponent } from "vue";

const logo = defineAsyncComponent(() => import("./logo.vue"));
const taskStats = defineAsyncComponent(() => import("./taskStats.vue"));
const priority = defineAsyncComponent(() => import("./priority.vue"));
const tag = defineAsyncComponent(() => import("./tag.vue"));
</script>

<style></style>
