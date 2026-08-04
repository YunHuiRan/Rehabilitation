<template>
  <svg
    width="24"
    height="24"
    viewBox="0 0 24 24"
    fill="none"
    xmlns="http://www.w3.org/2000/svg"
  >
    <rect
      x="4"
      y="3"
      width="16"
      height="18"
      rx="2"
      :stroke="iconColor"
      stroke-width="2"
    />
    <path
      d="M8 7H16"
      :stroke="iconColor"
      stroke-width="2"
      stroke-linecap="round"
    />
    <path
      d="M8 11H16"
      :stroke="iconColor"
      stroke-width="2"
      stroke-linecap="round"
    />
    <path
      d="M8 15H13"
      :stroke="iconColor"
      stroke-width="2"
      stroke-linecap="round"
    />
    <circle cx="17" cy="15" r="1" :fill="iconColor" />
  </svg>
</template>

<script setup lang="ts">
const iconColor = "#6364dd";
</script>
