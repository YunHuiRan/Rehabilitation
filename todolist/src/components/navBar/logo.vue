<template>
  <div class="h-6 flex flex-row justify-start items-center gap-4">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 64 64" class="w-8 h-8">
      <circle cx="32" cy="32" r="28" fill="var(--logo-circle-color)" />

      <path
        fill="var(--logo-check-color)"
        d="
      M 20 32
      L 27 39
      L 44 20
      L 46 22
      L 27 43
      L 18 34
      Z
    "
      />
    </svg>

    <h1 class="text-xl font-bold select-none">ToDo List</h1>
  </div>
</template>

<script setup lang="ts"></script>

<style></style>
