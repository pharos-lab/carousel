<template>
    <div class="slider">
        <slot></slot>
        <div class="controls">

        </div>
    </div>
</template>

<script setup>
import { provide, ref } from 'vue'

const props = defineProps({
    visible: Number,
})

const currentSlide = ref(0)

provide('slider', { currentSlide, visible: currentSlide.value + props.visible })
</script>