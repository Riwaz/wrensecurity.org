<script setup lang="ts">
import SectionTitle from './SectionTitle.vue';

defineProps<{
  title: string;
  description: string;
}>();
</script>

<template>
  <div class="wren-section-header">
    <SectionTitle :title="title" />
    <p>{{ description }}</p>
  </div>
</template>

<style scoped>
.wren-section-header .wren-section-title {
  flex: 1;
  border-top: none;
}

.wren-section-header p {
  flex: 1;
  margin: 0;
  margin-top: 32px;
}

@media (max-width: 768px) {
  .wren-section-header {
    flex-direction: column;
    row-gap: 16px;
  }
}
</style>
