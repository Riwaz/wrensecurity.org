<script setup lang="ts">
defineProps<{
  title: string;
}>();
</script>

<template>
  <h2 class="wren-section-title">{{ title }}</h2>
</template>

<style scoped>
.wren-section-title {
  margin: 0;
  font-size: 32px;
  line-height: 32px;
}

@media (max-width: 480px) {
  .wren-section-title {
    font-size: 28px;
    line-height: 28px;
  }
}
</style>
