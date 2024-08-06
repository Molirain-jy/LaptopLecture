<script setup lang="ts">
import { PropType, computed } from 'vue'
import Logo from './Logo.vue'
import { SNCLogoVariant } from '../types/SNCLogo'

const props = defineProps({
    ...Logo.props,
    variant: {
        type: String as PropType<SNCLogoVariant>,
        default: SNCLogoVariant.WithText,
    },
    src: undefined,
})

import imgWTextUrl from '../assets/images/SNC_logo_with_text.svg'
import imgWoTextUrl from '../assets/images/SNC_logo_without_text.svg'

const src = computed(() => {
    switch (props.variant) {
        case SNCLogoVariant.WithText:
            return imgWTextUrl
        case SNCLogoVariant.WithoutText:
            return imgWoTextUrl
    }
})

</script>

<template>
    <Logo v-bind="$props" :src="src" />
</template>
