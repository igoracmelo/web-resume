<script setup>

const links = [
  { icon: 'fa fa-whatsapp', url: 'htpp://wa.me/5599999999999', text: '+55 (99) 99999-9999' },
  { icon: 'fa fa-envelope-o', url: 'mailto:igoracm@outlook.com', text: 'igoracm@outlook.com' },
  { icon: 'fa fa-linkedin', url: 'https://www.linkedin.com/in/igoracmelo/', text: 'linkedin.com/in/igoracmelo' },
  { icon: 'fa fa-github', url: 'http://www.github.com/igoracmelo', text: 'github.com/igoracmelo' },
  { icon: 'fa fa-header', url: 'https://www.hackerrank.com/igoracmelo', text: 'hackerrank.com/igoracmelo' },
  { icon: 'fa fa-pencil-square-o', url: 'https://dev.to/tutorial_livre', text: 'dev.to/tutorial_livre' },
  { icon: 'fa fa-youtube-play', url: 'https://www.youtube.com/channel/UC7V4vg-lqAl40dpDQjxJg9w', text: 'Tutorial Livre' },
]

</script>

<template>
  <div class="links">
    <div class="link-btn" v-for="(link, i) in links" :key="i">
      <div class="link__icon"><i :class="link.icon"></i></div>
      <a class="link" target="_blank" :href="link.url">{{ link.text }}</a>
    </div>
  </div>
</template>

<style scoped lang="sass">
.links
  display: flex
  flex-direction: column
  align-items: center
  gap: 15px
  padding: 10px

  .link
    color: hsl(0 0 85%)

  .link-btn
    display: flex
    gap: 15px
    // align-items: center
    justify-content: center
    width: 100%
    max-width: 280px
    // text-align: center
    padding: 10px
    border-radius: 1000px
    background-color: hsl(0 0 30%)
    background-image: linear-gradient(45deg, hsl(0 0 30%), hsl(0 0 40%))
  // + *
  //   // border: 1px solid red
  //   margin-top: 10px

</style>