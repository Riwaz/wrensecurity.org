<script setup lang="ts">
withDefaults(
  defineProps<{
    columns?: number;
  }>(),
  {
    columns: 3
  }
);
</script>

<template>
  <div class="wren-feature-grid">
    <slot />
  </div>
</template>

<style scoped>
.wren-feature-grid {
  display: grid;
  grid-template-columns: repeat(v-bind(columns), 1fr);
  gap: 16px;
  margin-top: 48px;
}

@media (max-width: 960px) {
  .wren-feature-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 480px) {
  .wren-feature-grid {
    grid-template-columns: 1fr;
  }
}
</style>
