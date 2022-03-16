<template>
  <input :placeholder="placeholder" :class="classes" />
</template>

<script lang="ts" setup>
import { computed } from 'vue';

const props = defineProps<{
  placeholder: string;
}>();

const classes = computed(() => ({
  'px-2 py-1 rounded border border-gray-300 bg-white dark:bg-primary focus:border-pinkRed outline-none':
    true,
}));
</script>
