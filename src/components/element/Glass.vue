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
    position: relative;
    display: flex;
    padding: 14px 18px 18px 14px;
    display: inline-flex;
    border-radius: 6px;
    box-shadow: 3px 4px 5px rgba(darken($gray-3, 2.5%), 80%),
          inset -3px -4px 1px rgba(darken($gray-3, 10%), 80%),
          inset -3px -4px 25px rgba(darken($gray-3, 20%), 25%),
          inset -1.5px -2px 50px rgba($white, 25%),
          -3px -4px 10px rgba($white, 25%),
          3px 4px 10px rgba($white, 50%),
          inset 3px 4px 5px rgba(lighten($gray-3, 5%), 80%),
          -3px -4px 1px rgba(lighten($gray-3, 10%), 80%);
  }
}
</style>
