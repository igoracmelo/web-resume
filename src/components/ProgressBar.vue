<script setup>
import { defineProps } from 'vue'

const props = defineProps({
  progress: {
    required: true,
    type: Number
  }
})

</script>

<template>
  <div class="progress-bar">
    <div class="bar" :style="{ width: `${props.progress * 100}%`}"></div>
  </div>
</template>

<style scoped lang="sass">
.progress-bar
  height: 12px
  width: 150px
  min-width: 150px
  background-color: hsl(0, 0, 50%)

  .bar
    height: 100%
    background-color: hsl(0, 0, 70%)
</style>
