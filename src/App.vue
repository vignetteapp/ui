<script setup lang="ts">
import Input from '@/components/Input.vue';
import Button from './components/Button.vue';
</script>

<template>
  <div class="max-w-7xl mx-auto px-4 pt-20 gap-4">
    yo hi from vue
    <Input placeholder="lmao" />
    <Button size="small" primary>I'm a button lol</Button>

    <Button size="small">hi</Button>

    <Button size="medium">hi (medium)</Button>

    <Button size="large">hi (large)</Button>

    <Button size="large">hi here's a long long button lmao (large)</Button>

    <Button size="large" disabled>hi I'm disabled (large)</Button>
  </div>
</template>

<style>
@import '@/global.css';
</style>
