<template>
    <div class="slide" v-show="props.index < slider.visible">
        <slot></slot>
    </div>
</template>

<script setup>
import { inject, computed } from 'vue'

const props = defineProps({
    index: Number
})

const slider = inject('slider')

</script>