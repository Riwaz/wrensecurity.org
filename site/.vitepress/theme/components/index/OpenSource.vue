<script setup lang="ts">
import SectionHeader from '../common/SectionHeader.vue';
import type { OpenSourceItem } from '../../types/open-source-item';

defineProps<{
  title: string;
  description: string;
  items: OpenSourceItem[];
}>();
</script>

<template>
  <div class="wren-open-source">
    <SectionHeader :title="title" :description="description" />
    <p
      v-for="item in items"
      :key="item.label"
      class="wren-open-source-item"
    >
      <strong>{{ item.label }}:</strong> {{ item.description }}
    </p>
  </div>
</template>

<style scoped>
.wren-open-source {
  padding-top: 96px;
}

@media (max-width: 768px) {
  .wren-open-source {
    padding-top: 48px;
  }
}

.wren-open-source-item {
  margin: 32px 0 0;
}
</style>
