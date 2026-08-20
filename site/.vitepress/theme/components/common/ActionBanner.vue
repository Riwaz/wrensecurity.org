<script setup lang="ts">
import { VPButton } from 'vitepress/theme';
import SectionHeader from './SectionHeader.vue';
import type { Action } from '../../types/action';

const props = withDefaults(
  defineProps<{
    title: string;
    description: string;
    actions?: Action[];
    class?: string;
  }>(),
  {
    actions: () => [],
  }
);
</script>

<template>
  <div class="wren-action-banner" :class="props.class">
    <SectionHeader :title="title" :description="description" />
    <div v-if="actions.length" class="wren-action-banner-actions">
      <VPButton
        v-for="action in actions"
        :key="action.text"
        theme="alt"
        :text="action.text"
        :href="action.link"
      />
    </div>
    <div v-if="$slots.default" class="wren-action-banner-slot">
      <slot />
    </div>
  </div>
</template>

<style scoped>
.wren-action-banner {
  margin-top: 24px;
  padding: 48px;
  border-radius: 24px;
  background-color: var(--vp-c-brand-1);
}

.wren-action-banner-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  margin-top: 24px;
}

.wren-action-banner-slot {
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
