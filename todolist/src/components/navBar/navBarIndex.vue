<template>
  <div>
    <logo />
  </div>
</template>

<script setup lang="ts">
import { defineAsyncComponent } from "vue";

const logo = defineAsyncComponent(() => import("./logo.vue"));
</script>

<style></style>
