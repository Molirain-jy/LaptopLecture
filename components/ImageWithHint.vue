<script setup lang="ts">

const props = defineProps({
    alt: String,
    class: String,
    src: String,
})
</script>

<template>
    <div class="text-center w-fit">
        <img :src="src" :alt="alt" :class="class" />
        {{ props.alt }}
    </div>
</template>
