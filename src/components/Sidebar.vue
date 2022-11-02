<script setup>

import ProgressBar from './ProgressBar.vue';
import LinkList from './LinkList.vue';

// const links = [
//   { icon: 'fa fa-whatsapp', url: 'htpp://wa.me/5599999999999', text: '+55 (99) 99999-9999' },
//   { icon: 'fa fa-envelope-o', url: 'mailto:igoracm@outlook.com', text: 'igoracm@outlook.com' },
//   { icon: 'fa fa-linkedin', url: 'https://www.linkedin.com/in/igoracmelo/', text: 'linkedin.com/in/igoracmelo/' },
//   { icon: 'fa fa-github', url: 'http://www.github.com/igoracmelo', text: 'github.com/igoracmelo' },
//   { icon: 'fa fa-pencil-square-o', url: 'https://dev.to/tutorial_livre', text: 'dev.to/tutorial_livre' },
//   { icon: 'fa fa-youtube-play', url: 'https://www.youtube.com/channel/UC7V4vg-lqAl40dpDQjxJg9w', text: 'Tutorial Livre' },
// ]

const skills = [
  { name: 'Java', level: 0.8 },
  { name: 'JavaScript', level: 0.9 },
  { name: 'Node.js', level: 0.9 },
  { name: 'Go', level: 0.8 },
  { name: 'Vue.js', level: 0.8 },
  { name: 'CSS', level: 0.9 },
  { name: 'Clean Code', level: 0.8 },
  { name: 'SOLID', level: 0.7 },
  { name: 'Unit Tests', level: 0.8 },
  { name: 'MySQL', level: 0.8 },
  { name: 'Memory Management', level: 0.7 },
  { name: 'Linux', level: 0.8 },
]
</script>

<template>
  <!-- <div @click="collapseSidebar = !collapseSidebar" class="sidebar fx-col items-center" :class="{ 'collapse': collapseSidebar }"> -->
  <div class="sidebar floating fx-col items-center">
    <!-- <div class="toggle-collapse">
      <i class="fa fa-arrow-circle-right"></i>
    </div> -->
    <div class="avatar-container">
      <img src="/me.jpeg" alt="">
    </div>

    <div class="headings fx-col items-center g10">
      <div class="heading-name">Igor Melo</div>
      <div class="heading-headline">Full Stack Developer</div>
    </div>

    <div class="sidebar__hr"></div>

    <div class="sidebar__heading">Links and Contact</div>
    <link-list />

    <div class="sidebar__hr"></div>

    <div class="sidebar__heading">Skills self-evaluation</div>
    <div class="skill-briefs fx-col">
      <div class="skill-brief g10 fx-row items-center content-between w-full" v-for="(skill, i) in skills" :key="i">
        <div class="skill-brief__name">{{ skill.name }}</div>
        <progress-bar class="skill-brief__progress" :progress="skill.level"></progress-bar>
      </div>
    </div>
  </div>
</template>

<style scoped lang="sass">
// $bp-1: 1260px
// $bp-2: 1075px
@import '../styles/vars'

.heading-name
  font-size: 50px
  font-weight: bold

.heading-headline
  font-size: 30px

.sidebar
  $width: 350px
  width: $width
  min-width: $width
  min-height: 100vh
  color: white
  background-color: hsl(0 0 22%)
  background-image: linear-gradient(to right, hsl(0 0 22%), hsl(0 0 25%), hsl(0 0 22%))
  padding: 25px
  position: relative

  > *
    width: 100%
    max-width: 300px
    // text-align: center
  @media screen and (max-width: $bp-2)
    width: 100%

  // .toggle-collapse
  //   color: hsl(0 0 70%)
  //   filter: drop-shadow(0 1px 1px #000)
  //   position: absolute
  //   font-size: 35px
  //   left: calc($width + 10px)

  &__hr
    border-top: 5px solid hsl(0, 0, 40%)
    width: 50%
    margin: 40px 0

  &__heading
    text-align: center
    font-size: 20px
    font-weight: bold

.avatar-container
  border-radius: 50%
  width: 200px
  height: 200px
  overflow: hidden
  margin: 20px 0
  box-shadow: 0 10px 10px #0004
  border: 6px solid white

  img
    width: 100%

.contact-forms, .skill-briefs
  padding: 10px 0
  gap: 10px

</style>