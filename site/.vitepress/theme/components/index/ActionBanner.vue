<template>
  <div class="wren-action-banner">
    <div class="wren-section-header">
      <h2><slot name="title" /></h2>
      <p><slot name="description" /></p>
    </div>
    <div class="wren-action-banner-actions">
      <slot name="actions" />
    </div>
  </div>
</template>

<style scoped>
.wren-action-banner {
  margin-top: 96px;
  padding: 32px;
  border-radius: 24px;
  background-color: var(--vp-c-brand-1);
}

@media (max-width: 768px) {
  .wren-action-banner {
    margin-top: 48px;
  }
}

.wren-section-header h2 {
  padding-top: 0;
  color: var(--vp-c-bg-soft);
}

.wren-section-header p {
  margin-top: 16px;
  color: var(--vp-c-bg-soft);
}

.wren-action-banner-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  margin-top: 24px;
}
</style>
