<template>
  <div class="flex flex-col gap-6">
    <logo></logo>

    <taskStats></taskStats>

    <priority></priority>

    <tag></tag>

    <commonButton :button-icon="'+'" button-name="Add Task"></commonButton>
  </div>
</template>

<script setup lang="ts">
import { defineAsyncComponent } from "vue";

const logo = defineAsyncComponent(() => import("./logo.vue"));
const taskStats = defineAsyncComponent(() => import("./taskStats.vue"));
const priority = defineAsyncComponent(() => import("./priority.vue"));
const tag = defineAsyncComponent(() => import("./tag.vue"));

const commonButton = defineAsyncComponent(() => import("../commonButton.vue"));
</script>

<style></style>
