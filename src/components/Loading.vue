<template>
  <div
    v-if="loading"
    class="loading"
  >
    <LoadingIcon class="inline-block mb-1" />&nbsp;&nbsp;Carregando dados ...
    <div
      v-if="loadingError.tooLong"
      class="block mt-4"
    >
      Isso está demorando mais que o normal.
      <a href="/"> Reload? </a>
    </div>
  </div>
</template>

<script setup lang="ts">
import LoadingIcon from '@/assets/icons/loadingIcon.svg';
import { useStore } from '@/store/store';
import { storeToRefs } from 'pinia';
const { loading, loadingError } = storeToRefs(useStore());
</script>

<style lang="postcss" scoped>
.loading {
  @apply place-self-center text-center block;
}

a {
  @apply text-blue7 font-semibold text-center;
}
</style>
