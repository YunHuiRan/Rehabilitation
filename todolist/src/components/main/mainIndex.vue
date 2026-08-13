<template>
  <div class="flex flex-col gap-6">
    <taskHeader></taskHeader>

    <taskBreadcrumb></taskBreadcrumb>
  </div>
</template>

<script setup lang="ts">
import { defineAsyncComponent } from "vue";

const taskHeader = defineAsyncComponent(() => import("./taskHeader.vue"));
const taskBreadcrumb = defineAsyncComponent(
  () => import("./taskBreadcrumb.vue"),
);
</script>

<style></style>
