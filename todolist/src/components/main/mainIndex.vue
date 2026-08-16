<template>
  <div class="flex flex-col gap-6 h-full">
    <taskHeader></taskHeader>

    <taskItem></taskItem>
  </div>
</template>

<script setup lang="ts">
import { defineAsyncComponent } from "vue";

const taskHeader = defineAsyncComponent(() => import("./taskHeader.vue"));
const taskItem = defineAsyncComponent(() => import("./taskItem.vue"));
</script>

<style></style>
