<template>
  <button type="button" :class="classes" @click="onClick" :style="style">
    {{ label }}
  </button>
</template>

<script lang="ts" setup>
import { computed } from "vue";

const props = defineProps<{
  label: string;
  primary: boolean;
  size: "small" | "medium" | "large";
  backgroundColor: string;
}>();
defineEmits(["click"]);

const style = computed(() => ({
  backgroundColor: props.backgroundColor,
}));

const classes = computed(() => ({
  "text-4xl": true,
  "storybook-button--primary": props.primary,
  "storybook-button--secondary": !props.primary,
  [`storybook-button--${props.size || "medium"}`]: true,
}));
</script>
