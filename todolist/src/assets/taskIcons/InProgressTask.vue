<template>
  <svg
    width="24"
    height="24"
    viewBox="0 0 24 24"
    fill="none"
    xmlns="http://www.w3.org/2000/svg"
  >
    <circle
      cx="12"
      cy="12"
      r="9"
      :stroke="iconColor"
      stroke-width="1.8"
      opacity=".25"
    />

    <path
      d="M21 12A9 9 0 0 0 12 3"
      :stroke="iconColor"
      stroke-width="1.8"
      stroke-linecap="round"
    />

    <circle cx="12" cy="12" r="3" :fill="iconColor" />
  </svg>
</template>

<script setup lang="ts">
const iconColor = "#6364dd";
</script>
