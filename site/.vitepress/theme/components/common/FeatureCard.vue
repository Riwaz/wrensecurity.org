<script setup lang="ts">
import { withBase } from 'vitepress';
import Card from './Card.vue';

withDefaults(
  defineProps<{
    label?: string;
    title: string;
    description: string;
    link?: string;
    linkText?: string;
    variant?: 'soft' | 'outline';
  }>(),
  {
    variant: 'soft'
  }
);
</script>

<template>
  <Card class="wren-feature-card" :variant="variant">
    <span v-if="label" class="wren-feature-card-label">{{ label }}</span>
    <h3>{{ title }}</h3>
    <p>{{ description }}</p>
    <a v-if="link" class="wren-feature-card-link" :href="withBase(link)">{{ linkText }}</a>
  </Card>
</template>

<style scoped>
.wren-feature-card {
  display: flex;
  flex-direction: column;
}

.wren-feature-card-label {
  color: var(--vp-c-brand-1);
  margin-bottom: 16px;
  font-weight: 600;
}

.wren-feature-card h3 {
  margin: 0 0 16px;
  font-size: 18px;
}

.wren-feature-card p {
  flex: 1;
  margin: 0;
}

.wren-feature-card-link {
  margin-top: 12px;
  color: var(--vp-c-brand-1);
  font-weight: 500;
}

.wren-feature-card-link:hover {
  text-decoration: underline;
}

.wren-feature-card-link::after {
  content: " ->";
}
</style>
