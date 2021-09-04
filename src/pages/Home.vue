<script setup lang="ts">
import Banner from '@/components/layout/Banner.vue';
import Glass from '@/components/element/Glass.vue';
</script>

<template>
  <div id="home">
    <Banner :mode="'fullscreen'">
      <Glass>
        <div class="brand brand-title">
          <h1 class="brand-title--vertical">白羊</h1>
          <h2 class="brand-title--horizon">Aries Cs</h2>
        </div>
      </Glass>
    </Banner>
  </div>
</template>

<style lang="scss" scoped>
@import '@/assets/styles/shared';

.brand {
  &-title {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;

    &--vertical {
      writing-mode: vertical-rl;
      text-orientation: upright;
      font-size: 128px;
      letter-spacing: 72px;
      margin: 0;
      margin-bottom: -72px;
    }

    &--horizon {
      position: absolute;
      margin: 0;

      // Visual Fix
      margin-left: 0.325em;
    }
  }
}
</style>
