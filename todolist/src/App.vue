<template>
  <aside id="nav-bar-container">
    <navBarIndex />
  </aside>

  <main id="main-container">
    <mainIndex />
  </main>

  <aside id="overview-container">
    <overviewInfo />
  </aside>
</template>

<script setup lang="ts">
import { defineAsyncComponent } from "vue";

const navBarIndex = defineAsyncComponent(
  () => import("@/components/navBar/navBarIndex.vue"),
);

const mainIndex = defineAsyncComponent(
  () => import("@/components/main/mainIndex.vue"),
);

const overviewInfo = defineAsyncComponent(
  () => import("@/components/overviewInfo/overviewInfo.vue"),
);
</script>

<style></style>
