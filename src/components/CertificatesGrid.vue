<script setup>

const formatDate = (date) => {
  return 'Issued at ' + date.toLocaleString('default', {
    year: 'numeric',
    month: 'long'
  })
  // return `Issued at ${date.getMonth() + 1}/${date.getFullYear()}`
}

const certificates = [
  {
    title: "Go (Basic)",
    issuerName: "HackerRank",
    issuerImg: "hackerrank.jpeg",
    issuedDate: new Date(),
    url: "https://www.w3schools.com/tags/tag_progress.asp"
  },
  {
    title: "Advanced CSS and Sass: Flexbox, Grid, Animations and More!",
    issuerName: "Udemy",
    issuerImg: "udemy.jpeg",
    issuedDate: new Date(),
    url: "https://www.w3schools.com/tags/tag_progress.asp"
  },
]
</script>

<template>
  <div class="certificates-grid">
    <div class="certificate fx-col" v-for="(cert, i) in certificates" :key="i">
      <div class="fx-row g10">
        <img :src="cert.issuerImg" class="certificate__issuer-img" :title="cert.issuerName" />
        <div class="certificate__title">
          {{ cert.title }}
        </div>
      </div>
      <div class="fx-row content-between items-center">
        <div class="certificate__date">{{ formatDate(cert.issuedDate) }}</div>
        <a target="_blank" :href="cert.url" class="certificate__view">View credential →</a>
      </div>
    </div>
  </div>
</template>

<style scoped lang="sass">

.certificates-grid
  display: grid
  grid-template-columns: repeat(2, 1fr)
  gap: 25px

.certificate
  // border: 1px solid red
  box-shadow: 0 2px 7px #0003
  padding: 15px
  gap: 20px

  &__title
    font-size: 20px

  &__issuer-img
    width: 50px
    height: 50px
    border-radius: 25%

  &__view
    color: #000c
    padding: 7px 13px
    border: 1px solid #000c
    border-radius: 1000px
    text-align: center
</style>