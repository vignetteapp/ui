<template>
  <button type="button" :class="classes" :style="style">
    <slot></slot>
  </button>
</template>

<script lang="ts" setup>
import { computed } from "vue";

const props = defineProps<{
  primary?: boolean;
  size: "small" | "medium" | "large";
  disabled?: boolean
  backgroundColor?: string;
}>();
defineEmits(["click"]);

const style = computed(() => ({
  backgroundColor: props.backgroundColor,
}));

const classes = computed(() => ({
  "rounded-full px-10 duration-100 transition py-2 font-bold text-white shadow outline-none": true,
  "bg-pinkRed hover:bg-[#ff2277]": props.primary && !props.disabled,
  "bg-neutral-500 text-gray-300 cursor-not-allowed": props.disabled,
  "bg-black hover:bg-neutral-700 text-white rounded-full":
    !props.primary && !props.disabled,
  'text-xl ': props.size == 'large',
  'text-sm': props.size == 'medium',
  'text-xs': props.size == 'small',


}));
</script>
