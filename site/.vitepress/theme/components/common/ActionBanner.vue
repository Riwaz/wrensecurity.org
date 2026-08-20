<script setup lang="ts">
withDefaults(
  defineProps<{
    variant?: 'brand' | 'outline' | 'soft';
  }>(),
  {
    variant: 'brand'
  }
);
</script>

<template>
  <div class="wren-action-banner" :class="`wren-action-banner-${variant}`">
    <div class="wren-section-header">
      <h2><slot name="title" /></h2>
      <p><slot name="description" /></p>
    </div>
    <div class="wren-action-banner-actions">
      <slot name="actions" />
    </div>
    <div v-if="$slots.default" class="wren-action-banner-slot">
      <slot />
    </div>
  </div>
</template>

<style scoped>
.wren-action-banner {
  margin-top: 96px;
  padding: 32px;
  border-radius: 24px;
}

@media (max-width: 768px) {
  .wren-action-banner {
    margin-top: 48px;
  }
}

.wren-action-banner-brand {
  background-color: var(--vp-c-brand-1);
}

.wren-action-banner-outline {
  background-color: transparent;
  border: 2px solid var(--vp-c-brand-1);
}

.wren-action-banner-soft {
  background-color: var(--vp-c-bg-soft);
}

.wren-section-header h2 {
  padding-top: 0;
}

.wren-section-header p {
  margin-top: 16px;
}

.wren-action-banner-brand .wren-section-header h2,
.wren-action-banner-brand .wren-section-header p {
  color: var(--vp-c-bg-soft);
}

.wren-action-banner-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  margin-top: 24px;
}

.wren-action-banner-slot {
  margin-top: 24px;
}
</style>
