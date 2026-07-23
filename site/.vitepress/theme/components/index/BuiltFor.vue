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
  <div class="wren-built-for">
    <SectionHeader :title="title" :description="description" />
    <FeatureGrid>
      <FeatureCard
        v-for="item in items"
        :key="item.label"
        v-bind="item"
      />
    </FeatureGrid>
  </div>
</template>

<style scoped>
.wren-built-for {
  padding-top: 96px;
}

@media (max-width: 768px) {
  .wren-built-for {
    padding-top: 48px;
  }
}
</style>
