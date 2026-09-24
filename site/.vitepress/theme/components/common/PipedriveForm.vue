<script setup lang="ts">
import { onMounted } from 'vue';

const props = defineProps<{
  formUrl: string;
}>();

const LOADER_SRC = 'https://webforms.pipedrive.com/f/loader';

onMounted(() => {
  // Re-add the Pipedrive loader on every mount, otherwise it renders forms only on full page load.
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
