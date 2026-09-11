<script setup lang="ts">
const props = withDefaults(
  defineProps<{
    columns?: number;
    class?: string;
  }>(),
  {
    columns: 3
  }
);
</script>

<template>
  <div class="wren-card-grid" :class="props.class">
    <slot />
  </div>
</template>

<style scoped>
.wren-card-grid {
  display: grid;
  grid-template-columns: repeat(v-bind(columns), 1fr);
  gap: 16px;
  margin-top: 48px;
}

@media (max-width: 960px) {
  .wren-card-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 640px) {
  .wren-card-grid {
    grid-template-columns: 1fr;
  }
}
</style>
