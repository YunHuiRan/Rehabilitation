<template>
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1024 1024">
    <path
      :fill="iconColor"
      d="M256 128v698.88l196.032-156.864a96 96 0 0 1 119.936 0L768 826.816V128zm-32-64h576a32 32 0 0 1 32 32v797.44a32 32 0 0 1-51.968 24.96L531.968 720a32 32 0 0 0-39.936 0L243.968 918.4A32 32 0 0 1 192 893.44V96a32 32 0 0 1 32-32"
    ></path>
  </svg>
</template>

<script setup lang="ts">
let iconColor:
  | "var(--high-priority-color)"
  | "var(--medium-priority-color)"
  | "var(--low-priority-color)";

const props = defineProps<{
  level: "high" | "medium" | "low";
}>();

switch (props.level) {
  case "high":
    iconColor = "var(--high-priority-color)";
    break;
  case "medium":
    iconColor = "var(--medium-priority-color)";
    break;
  case "low":
    iconColor = "var(--low-priority-color)";
    break;
}
</script>
