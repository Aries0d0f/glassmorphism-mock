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

#home {
  background: linear-gradient(120deg, $gray-6, $gray-5);
  background-position: 15% 25%;
}

.brand {
  &-title {
    position: relative;
    display: flex;
    width: 128px;
    justify-content: center;
    align-items: center;
    text-shadow: 1px 2px 2px rgba(darken($gray-1, 5%), 25%),
        -1px -2px 2px rgba(lighten($gray-1, 50%), 25%);

    &--vertical,
    &--horizon {
      filter: blur(0.4pt);
    }

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
      white-space: nowrap;
    }
  }
}
</style>
