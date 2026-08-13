<template>
  <div class="">
    <taskHeader></taskHeader>
  </div>
</template>

<script setup lang="ts">
import { defineAsyncComponent } from "vue";

const taskHeader = defineAsyncComponent(() => import("./taskHeader.vue"));
</script>

<style></style>
