<script setup lang="ts">
import { defineProps, withDefaults } from 'vue';

const props = withDefaults(
  defineProps<{
    mode?: 'default' | 'fullscreen';
  }>(),
  {
    mode: 'default'
  }
);
</script>

<template>
  <div class="banner banner-container" :class="{ fullscreen: mode === 'fullscreen' }">
    <slot />
  </div>
</template>

<style lang="scss" scoped>
@import '@/assets/styles/shared';

.banner {
  &-container {
    position: relative;
    display: flex;
    width: 100%;
    justify-content: center;
    align-items: center;

    &.fullscreen {
      min-height: 100vh;
    }
  }
}
</style>
