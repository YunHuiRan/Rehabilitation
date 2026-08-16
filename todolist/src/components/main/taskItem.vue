<template>
  <div class="w-full h-full flex flex-col gap-2 pr-3 overflow-auto">
    <!-- task item -->
    <div v-for="_ in 5" class="w-full h-24 flex gap-2 flex-row">
      <!-- task info -->
      <div
        class="h-full grow-5 flex justify-center items-start flex-col max-w-1/2"
      >
        <h1 class="h-1/2 text-2xl flex items-center">title</h1>
        <h2 class="h-1/2 opacity-50 overflow-hidden text-ellipsis">
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Nemo
          perspiciatis delectus quibusdam aliquam, illo, nostrum quis unde
          fugiat ullam sit quos possimus cumque, fugit ratione porro a provident
          veritatis perferendis!
        </h2>
      </div>

      <!-- task status -->
      <div class="h-full grow-3 flex justify-center items-center bg-blue-300">
        <commonSwticher></commonSwticher>
      </div>

      <!-- task edit -->
      <div class="h-full grow-2 bg-blue-300"></div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineAsyncComponent } from "vue";

const commonSwticher = defineAsyncComponent(
  () => import("@/components/commonSwticher.vue"),
);
</script>

<style></style>
