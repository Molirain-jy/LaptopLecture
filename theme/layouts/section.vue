<script setup lang="ts">
import SlideLogo from '../components/SlideLogo.vue'

const props = defineProps({
  ...SlideLogo.props,
})
</script>

<template>
  <div class="slidev-layout section w-full h-full grid">
    <div class="my-auto text-center">
      <SlideLogo v-bind="$props" />
      <slot />
    </div>
  </div>
</template>
