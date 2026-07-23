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
  <div class="wren-building-blocks">
    <SectionHeader :title="title" :description="description" />
    <FeatureGrid>
      <FeatureCard
        v-for="item in items"
        :key="item.link"
        v-bind="item"
      />
      <!-- The card will be added later after content will be created for it. -->
      <!-- <FeatureCard variant="outline" v-bind="callout" /> -->
    </FeatureGrid>
  </div>
</template>

<style scoped>
.wren-building-blocks {
  padding-top: 96px;
}

@media (max-width: 768px) {
  .wren-building-blocks {
    padding-top: 48px;
  }
}
</style>
