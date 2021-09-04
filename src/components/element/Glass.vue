<script setup lang="ts"></script>

<template>
  <div class="glass glass-container">
    <slot />
  </div>
</template>

<style lang="scss" scoped>
@import '@/assets/styles/shared';

.glass {
  &-container {
    padding: 16px;
    display: inline-flex;
  }
}
</style>
