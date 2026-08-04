<template>
  <button
    class="common-button"
    :style="{
      width: props.width ? props.width : '',
      height: props.height ? props.height : '',
      backgroundColor: props.bgColor ? props.bgColor : 'var(--primary-color)',
      color: props.color ? props.color : 'white',
    }"
  >
    <slot name="buttonIcon">{{ props.buttonIcon }} </slot>

    <slot name="buttonName">{{ props.buttonName }}</slot>
  </button>
</template>

<script setup lang="ts">
const props = defineProps<{
  buttonName: string;
  buttonIcon?: string;
  width?: string;
  height?: string;
  color?: string;
  bgColor?: string;
}>();
</script>

<style scoped>
.common-button {
  padding: 0.5rem 1rem;
  border-radius: 0.5rem;
  font-size: 1rem;
  transition: var(--item-transiton);
}

.common-button:hover {
  cursor: pointer;
  box-shadow: var(--card-shadow);
}
</style>
