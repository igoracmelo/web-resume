<script setup>

const formatDate = (date) => {
  return 'Issued at ' + date.toLocaleString('en-US', {
    year: 'numeric',
    month: 'long'
  })
}

const certificates = [
  {
    title: "Go (Basic)",
    issuerName: "HackerRank",
    issuerImg: "hackerrank.jpeg",
    issuedDate: new Date("2022-09-26"),
    url: "https://www.hackerrank.com/certificates/44233dac2d31"
  },
  {
    title: "JavaScript (Basic)",
    issuerName: "HackerRank",
    issuerImg: "hackerrank.jpeg",
    issuedDate: new Date("2022-11-02"),
    url: "https://www.hackerrank.com/certificates/4df7ba9bb77b"
  },
  {
    title: "SQL (Basic)",
    issuerName: "HackerRank",
    issuerImg: "hackerrank.jpeg",
    issuedDate: new Date("2022-11-02"),
    url: "https://www.hackerrank.com/certificates/bb4cca58f57d"
  },
  {
    title: "Node (Basic)",
    issuerName: "HackerRank",
    issuerImg: "hackerrank.jpeg",
    issuedDate: new Date("2022-11-02"),
    url: "https://www.hackerrank.com/certificates/bb4cca58f57d"
  },
  {
    title: "Git - Básico ao avançado",
    issuerName: "Udemy",
    issuerImg: "udemy.jpeg",
    issuedDate: new Date("2022-03-02"),
    url: "https://www.w3schools.com/tags/tag_progress.asp"
  },
  {
    title: "Advanced CSS and Sass: Flexbox, Grid, Animations and More!",
    issuerName: "Udemy",
    issuerImg: "udemy.jpeg",
    issuedDate: new Date("2021-06-02"),
    url: "https://www.w3schools.com/tags/tag_progress.asp"
  },
  {
    title: "Curso Desenvolvedor Web Completo + 10 projetos",
    issuerName: "Udemy",
    issuerImg: "udemy.jpeg",
    issuedDate: new Date("2020-04-02"),
    url: "https://www.w3schools.com/tags/tag_progress.asp"
  },
]
</script>

<template>
  <div class="certificates-grid">
    <div class="certificate fx-col content-between" v-for="(cert, i) in certificates" :key="i">
      <div class="fx-row g10">
        <img :src="cert.issuerImg" class="certificate__issuer-img" :title="cert.issuerName" />
        <div class="certificate__title">
          {{ cert.title }}
        </div>
      </div>
      <div class="fx-row content-between items-center">
        <div class="certificate__date">{{ formatDate(cert.issuedDate) }}</div>
        <a target="_blank" :href="cert.url" class="certificate__view">credential →</a>
      </div>
    </div>
  </div>
</template>

<style scoped lang="sass">

.certificates-grid
  display: grid
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr))
  gap: 25px

.certificate
  box-shadow: 0 2px 7px #0003
  padding: 15px
  gap: 20px

  &__title
    font-size: 20px

  &__date
    font-size: 15px

  &__issuer-img
    width: 50px
    height: 50px
    border-radius: 25%

  &__view
    color: #000c
    font-size: 15px
    padding: 7px 13px
    border: 1px solid #000c
    border-radius: 1000px
    text-align: center
</style>