<script setup lang="ts">
import { withBase } from 'vitepress';
import Card from '../common/Card.vue';
import type { Partner } from '../../types/partner';

withDefaults(
  defineProps<{
    partner: Partner;
    variant?: 'soft' | 'outline' | 'outline-soft';
  }>(),
  {
    variant: 'soft'
  }
);

function websiteLabel(url: string): string {
  return new URL(url).hostname.replace(/^www\./, '');
}
</script>

<template>
  <Card class="wren-partner-card" :variant="variant">
    <h3>{{ partner.name }}</h3>
    <div class="wren-partner-card-details">
      <p>Web: <a :href="partner.url" target="_blank" rel="noopener">{{ websiteLabel(partner.url) }}</a></p>
      <p v-if="partner.email">E-mail: <a :href="`mailto:${partner.email}`">{{ partner.email }}</a></p>
      <p v-if="partner.region">Region: {{ partner.region }}</p>
    </div>
    <div class="wren-partner-card-logo">
      <img :src="withBase('partner/' + partner.logo)" :alt="partner.name">
    </div>
  </Card>
</template>

<style scoped>
.wren-partner-card {
  display: flex;
  flex-direction: column;
}

.wren-partner-card h3 {
  margin: 0 0 16px;
  font-size: 18px;
  line-height: 18px;
}

.wren-partner-card-details {
  flex: 1;
}

.wren-partner-card-details p {
  margin: 0;
}

.wren-partner-card-logo {
  margin-top: 24px;
}

.wren-partner-card-logo img {
  max-height: 40px;
  max-width: 50%;
  margin: 0;
}
</style>
