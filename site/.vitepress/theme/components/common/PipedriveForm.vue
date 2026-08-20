<script setup lang="ts">
import { onMounted } from 'vue';

const props = defineProps<{
  formUrl: string;
}>();

const LOADER_SRC = 'https://webforms.pipedrive.com/f/loader';

onMounted(() => {
  // The loader only scans the DOM for .pipedriveWebForms once, on script
  // insertion — it has no MutationObserver, so it must be re-inserted (and
  // re-executed) on every mount to pick up the form after SPA navigation.
  document.querySelectorAll('script[data-pipedrive-loader]').forEach((el) => el.remove());
  const script = document.createElement('script');
  script.src = LOADER_SRC;
  script.setAttribute('data-pipedrive-loader', '');
  document.body.appendChild(script);
});
</script>

<template>
  <div class="pipedriveWebForms" :data-pd-webforms="props.formUrl"></div>
</template>
