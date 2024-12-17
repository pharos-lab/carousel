<template>
    <div class="slide bg-slate-300" v-show="showSlide">
        <slot></slot>
    </div>
</template>

<script setup>
import { inject, computed } from 'vue'

const props = defineProps({
    index: Number
})

const slider = inject('slider')

const showSlide = computed(() => {
    return props.index < slider.visible && props.index >= slider.currentSlide.value
})

const size = computed(() => {
    return 100/ slider.slideProp.visible + '%'
})

</script>

<style>
.slide {
    width: v-bind(size);
}
</style>