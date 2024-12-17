<template>
    <div class="slider relative flex gap-4">
        <slot></slot>
        <div class="controls absolute top-1/2 bg-slate-500">

        </div>
    </div>
</template>

<script setup>
import { provide, ref } from 'vue'

const props = defineProps({
    visible: Number,
})

const currentSlide = ref(0)

provide('slider', { currentSlide, visible: currentSlide.value + props.visible, slideProp: props })
</script>