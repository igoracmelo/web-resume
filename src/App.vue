<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
</script>

<template>
  <div class="container fx-row">
    <div class="sidebar fx-col items-center">
      <div class="avatar-container">
        <img src="/me.jpeg" alt="">
      </div>

      <div class="sidebar__heading">Links</div>
      <div class="links fx-col">
        <div class="link fx-row" v-for="i in 3" :key="i">
          <div class="link__icon">(GH)</div>
          <div class="link__description">GitHub: </div>
          <a class="link__anchor" href="http://github.com/igoracmelo">github.com/igoracmelo</a>
        </div>
      </div>

      <div class="sidebar__hr"></div>

      <div class="sidebar__heading">Contact</div>
      <div class="contact-forms fx-col">
        <div class="contact fx-row" v-for="i in 3" :key="i">
          <div class="contact__icon">(TEL)</div>
          <!-- <div class="contact__description">GitHub: </div> -->
          <a href="http://github.com/igoracmelo">+55 (99) 99999-9999</a>
        </div>
      </div>

      <div class="sidebar__hr"></div>

      <div class="sidebar__heading">Skills brief</div>
      <div class="skill-briefs fx-col">
        <div class="skill-brief fx-row" v-for="i in 3" :key="i">
          <div class="skill-brief__name">English</div>
          <progress class="skill-brief__progress" value="0.7"></progress>
        </div>
      </div>
    </div>
    <main class="main">
      <div class="idk fx-col">
        <div class="heading-name">Igor Melo</div>
        <div class="heading-headline">Full Stack Developer</div>
      </div>

      <div class="main__heading">Certificates</div>
      <div class="certificates-grid">
        <div class="certificate fx-col" v-for="i in 3" :key="i">
          <div class="fx-row g10">
            <img src="/hackerrank.jpeg" class="certificate__issuer-img" />
            <div class="certificate__title">
              Advanced CSS and Sass: Flexbox, Grid, Animations and More!
            </div>
          </div>
          <div class="fx-row content-between items-center">
            <div class="certificate__date">Issued on Jun 2022</div>
            <a href="#" class="certificate__view">View credential →</a>
          </div>
        </div>
        <!-- <div class="certificate__issuer">
          Udemy
        </div> -->
        <!-- <div class="certificate">certificate</div> -->
      </div>
    </main>
  </div>
  <!-- <div class="fx-row">
  </div> -->
</template>

<style lang="sass">
*
  box-sizing: border-box
  padding: 0
  margin: 0
  font-family: arial

.certificates-grid
  display: grid
  grid-template-columns: repeat(2, 1fr)
  gap: 25px

.certificate
  border: 1px solid red
  // height: 200px
  padding: 15px
  gap: 20px

  &__title
    font-size: 20px

  &__issuer-img
    width: 50px
    height: 50px
    border-radius: 25%

  &__view
    padding: 7px 20px
    border: 1px solid red
    border-radius: 1000px
    text-align: center
    // width: 200px

.g10
  gap: 10px

.main
  width: 100%
  padding: 40px

  &__heading
    font-size: 30px
    font-weight: bold
    padding: 20px 0
    display: flex
    align-items: center
    gap: 30px

    &::after
      content: ""
      display: block
      flex: 1
      border-top: 1px solid black

.skill-brief
  gap: 10px

.sidebar
  width: 350px
  min-width: 350px
  min-height: 100vh
  border: 1px solid #000

  &__hr
    border-top: 1px solid #000
    width: 90%
    margin: 30px 0

.fx-row
  display: flex

.fx-col
  display: flex
  flex-direction: column

.sidebar__heading
  // padding: 20px 0
  font-size: 20px
  font-weight: bold

.links, .contact-forms, .skill-briefs
  padding: 10px 0
  gap: 10px

.link
  gap: 5px

.content-between
  justify-content: space-between

.content-center
  justify-content: center

.items-center
  align-items: center

.avatar-container
  border-radius: 50%
  width: 200px
  height: 200px
  overflow: hidden
  margin: 30px 0

  img
    width: 100%

.heading-name
  font-size: 50px
  font-weight: bold

.heading-headline
  font-size: 30px

</style>
