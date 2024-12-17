<template>
  <div class="p-4 bg-slate-100">

    <Slider :visible="2" class="bg-slate-200">
      <Slide :index="0">ok 0</Slide>
      <Slide :index="1">ok 1</Slide>
      <Slide :index="2">ok 2</Slide>
      <Slide :index="3">ok 3</Slide>
      <Slide :index="4">ok 4</Slide>
      <Slide :index="5">ok 5</Slide>
      <Slide :index="6">ok 6</Slide>
    </Slider>
  </div>
 
</template>

<script setup>
import Slider from './components/Slider.vue'
import Slide from './components/Slide.vue'
</script>

<style scoped>

</style>
