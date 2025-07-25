<template>
  <svg
    :width="width"
    :height="height"
    viewBox="0 0 40 40"
    fill="none"
    xmlns="http://www.w3.org/2000/svg"
  >
    <path
      d="M20 35C28.2843 35 35 28.2843 35 20C35 11.7157 28.2843 5 20 5C11.7157 5 5 11.7157 5 20C5 28.2843 11.7157 35 20 35Z"
      :stroke="secondaryColor"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
    <path
      d="M14.7031 19.0469L20 13.75L25.2969 19.0469"
      :stroke="color"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
    <path
      d="M20 26.25V13.75"
      :stroke="color"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
  </svg>
</template>

<script setup lang="ts">
const {
  width = 48,
  height = 48,
  color = "#fff",
  secondaryColor = "#E4F4F4"
} = defineProps<{
  color?: string;
  secondaryColor?: string;
  width?: number;
  height?: number;
}>();
</script>
