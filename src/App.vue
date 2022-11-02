<script setup>

import { ref } from 'vue'
import CertificatesGrid from './components/CertificatesGrid.vue';
import Experiences from './components/Experiences.vue';
import Sidebar from './components/Sidebar.vue';

const collapseSidebar = ref(false)
// const sidebar = ref(null)

// const toggleSidebar = () => {
//   collapseSidebar.value = !collapseSidebar.value
// }
</script>

<template>
  <div class="app">
    <div class="resume fx-row">
      <sidebar />
      <main class="main">
        <!-- <p>
          I'm passionate about computer science since I was 13.<br>
          I really enjoy what I do and it's both a job and a hobbie.<br>
        </p>
        <p>
          I study every day, always seeking to know more and to be a better professional.
        </p> -->
        <div class="main__heading">Experiences</div>
        <experiences />

        <div class="main__heading">Certificates</div>
        <certificates-grid />
      </main>
    </div>
  </div>
</template>

<style lang="sass">
@import './styles/vars'

.app
  width: 100%
  // height: 100vh
  display: flex
  justify-content: center
  background-color: hsl(0, 0, 75%)

.resume
  // width: 100vw
  position: relative
  height: 100%
  margin: 30px 0
  width: 100vw
  max-width: 1200px
  background-color: white
  box-shadow: 0 0 15px #0004
  @media screen and (max-width: $bp-1)
    max-width: 100vw
    margin: 0

  @media screen and (max-width: $bp-2)
    flex-direction: column

.main
  width: 100%
  padding: 30px 50px
  display: flex
  flex-direction: column
  align-items: center

  > *
    width: 100%
    max-width: 650px

  &__heading
    font-size: 30px
    font-weight: bold
    padding: 20px 0
    display: flex
    align-items: center
    gap: 30px

    &::before
      content: ""
      display: block
      flex: 1
      border-top: 1px solid black

    &::after
      content: ""
      display: block
      flex: 1
      border-top: 1px solid black

</style>
