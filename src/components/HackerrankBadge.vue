<script setup>

import { defineProps } from 'vue'

const props = defineProps({
  image: {
    required: true,
    type: String
  },
  title: {
    required: true,
    type: String
  },
  stars: {
    default: 0,
    type: Number
  },
  color: String
})

</script>

<template>
  <a href="https://www.hackerrank.com/igoracmelo" target="_blank" class="hr-badge" :class="props.color">
    <div class="image">
      <img :src="props.image" alt="">
    </div>
    <div class="title">{{ props.title }}</div>
    <div class="stars">
      <i class="fa fa-star" v-for="i in props.stars"></i>
    </div>
  </a>
</template>

<style scoped lang="sass">

.hr-badge
  --color: silver
  // padding: 15px 10px
  width: 120px
  height: 120px
  // border: 1px solid red
  display: flex
  flex-direction: column
  align-items: center
  justify-content: center
  gap: 5px
  color: hsl(0, 0, 20%)
  // color: red
  background-color: var(--color)
  background-image: linear-gradient(135deg, hsla(0, 0, 100%, 30%), hsla(0, 0, 0%, 10%))
  border-radius: 30%

  &.silver
    --color: hsl(180deg, 30%, 90%)
  &.gold
    --color: gold


.image
  // width: 45%
  padding: 10px
  img
    opacity: 0.9
    width: 30px
    // width: 100%

.title
  font-size: 12px
  font-weight: bold

.stars
  display: flex
  font-size: 10px
  gap: 2px
  opacity: 0.9
  // color: inherit

</style>