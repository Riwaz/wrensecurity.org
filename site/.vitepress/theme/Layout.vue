<script setup lang="ts">
import DefaultTheme from 'vitepress/theme';

const { Layout } = DefaultTheme;
</script>

<template>
  <Layout>
    <template #home-hero-info-before>
      <p class="hero-topnote">Open by default · Secure by design · Crafted to last</p>
    </template>
  </Layout>
</template>

<style scoped>
.hero-topnote {
  margin-bottom: 8px;
  font-weight: 500;
}

</style>