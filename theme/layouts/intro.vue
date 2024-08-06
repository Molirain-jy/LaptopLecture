<script setup lang="ts">
import SlideLogo from '../components/SlideLogo.vue'

const props = defineProps({
  ...SlideLogo.props,
})
</script>

<template>
  <div class="slidev-layout intro">
    <div class="my-auto">
      <SlideLogo v-bind="$props" />
      <slot />
    </div>
  </div>
</template>
