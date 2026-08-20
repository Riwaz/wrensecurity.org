<script setup lang="ts">
withDefaults(
  defineProps<{
    variant?: 'soft' | 'outline';
  }>(),
  {
    variant: 'soft'
  }
);
</script>

<template>
  <div class="wren-card" :class="`wren-card-${variant}`">
    <slot />
  </div>
</template>

<style scoped>
.wren-card {
  border-radius: 16px;
  padding: 24px;
}

.wren-card-soft {
  background-color: var(--vp-c-bg-soft);
}

.wren-card-outline {
  background-color: transparent;
  border: 2px solid var(--vp-c-brand-1);

}
</style>
