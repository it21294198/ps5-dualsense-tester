<script setup lang="ts">
import type { ModelProps } from '@/device-based-router/shared'
import DSBack from './_ModelPanel/DSBack.vue'
import DSBody from './_ModelPanel/DSBody.vue'
import DSCover from './_ModelPanel/DSCover.vue'

defineProps<ModelProps>()
</script>

<template>
  <div class="relative w-full">
    <svg viewBox="0 0 1117 892">
      <!-- placeholder -->
    </svg>
    <svg class="model" viewBox="0 0 1117 892">
      <DSBack :show-value="showValue" />
    </svg>
    <svg v-once class="model" viewBox="0 0 1117 892">
      <DSBody />
    </svg>
    <svg class="model" viewBox="0 0 1117 892">
      <DSCover :show-value="showValue" />
    </svg>
  </div>
</template>

<style scoped>
svg {
  @apply w-full;
}

svg.model {
  @apply w-full absolute top-0 left-0;
}
</style>
