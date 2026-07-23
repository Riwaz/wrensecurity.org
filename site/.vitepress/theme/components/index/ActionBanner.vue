<script setup lang="ts">
import { VPButton } from 'vitepress/theme';
import SectionHeader from '../common/SectionHeader.vue';
import type { Action } from '../../types/action';

defineProps<{
  title: string;
  description: string;
  actions: Action[];
}>();
</script>

<template>
  <div class="wren-action-banner">
    <SectionHeader :title="title" :description="description" />
    <div class="wren-action-banner-actions">
      <VPButton
        v-for="action in actions"
        :key="action.text"
        theme="alt"
        :text="action.text"
        :href="action.link"
      />
    </div>
  </div>
</template>

<style scoped>
.wren-action-banner {
  margin-top: 96px;
  padding: 48px;
  border-radius: 24px;
  background-color: var(--vp-c-brand-1);
}

@media (max-width: 768px) {
  .wren-action-banner {
    margin-top: 48px;
  }
}

.wren-action-banner-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  margin-top: 24px;
}
</style>

<style>
.wren-action-banner .wren-section-title {
  color: var(--vp-c-bg-soft);
  padding-top: 0;
}

.wren-action-banner .wren-section-header p {
  color: var(--vp-c-bg-soft);
  margin-top: 16px;
}
</style>
