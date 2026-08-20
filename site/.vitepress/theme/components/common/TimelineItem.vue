<template>
  <div class="wren-timeline-item">
    <div class="wren-timeline-marker">
      <span class="wren-timeline-dot" />
      <span class="wren-timeline-line" />
    </div>
    <div class="wren-timeline-content">
      <span v-if="$slots.label" class="wren-timeline-label"><slot name="label" /></span>
      <h3><slot name="title" /></h3>
      <p><slot name="description" /></p>
    </div>
  </div>
</template>

<style scoped>
.wren-timeline-item {
  display: flex;
  gap: 48px;
}

@media (max-width: 480px) {
  .wren-timeline-item {
    gap: 24px;
  }
}

.wren-timeline-marker {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.wren-timeline-dot {
  width: 16px;
  height: 16px;
  margin-top: 4px;
  border-radius: 50%;
  background-color: var(--vp-c-brand-1);
}

.wren-timeline-line {
  flex: 1;
  width: 2px;
  margin-top: 4px;
  background-color: var(--vp-c-brand-1);
}

.wren-timeline-item:last-child .wren-timeline-line {
  display: none;
}

.wren-timeline-content {
  padding-bottom: 48px;
}

.wren-timeline-item:last-child .wren-timeline-content {
  padding-bottom: 0;
}

.wren-timeline-label {
  display: block;
  color: var(--vp-c-brand-1);
  font-weight: 600;
  margin-bottom: 8px;
}

.wren-timeline-content h3 {
  margin: 0 0 8px;
  padding-top: 0;
  border-top: none;
  font-size: 18px;
}

.wren-timeline-content p {
  margin: 0;
}
</style>
