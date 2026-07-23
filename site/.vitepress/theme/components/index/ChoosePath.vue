<script setup lang="ts">
import SectionHeader from '../common/SectionHeader.vue';
import FeatureGrid from '../common/FeatureGrid.vue';
import FeatureCard from '../common/FeatureCard.vue';
import type { Feature } from '../../types/feature';

defineProps<{
  title: string;
  description: string;
  items: Feature[];
}>();
</script>

<template>
  <div class="wren-choose-path">
    <SectionHeader :title="title" :description="description" />
    <FeatureGrid class="wren-choose-path-grid">
      <FeatureCard
        v-for="item in items"
        :key="item.label"
        variant="outline"
        v-bind="item"
      />
    </FeatureGrid>
  </div>
</template>

<style scoped>
.wren-choose-path {
  padding-top: 96px;
}

@media (max-width: 768px) {
  .wren-choose-path {
    padding-top: 48px;
  }
}
</style>
