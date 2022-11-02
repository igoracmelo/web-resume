<script setup>

const formatDate = (date) => {
  // 'Issued at '
  return date.toLocaleString('en-US', {
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
    url: "https://www.hackerrank.com/certificates/47a0cc46fe09"
  },
  {
    title: "Git - From basic to advanced",
    issuerName: "Udemy",
    issuerImg: "udemy.jpeg",
    issuedDate: new Date("2022-03-02"),
    url: "https://www.udemy.com/certificate/UC-1b20e3e9-df16-4601-a6f9-5effa7df9117/"
  },
  {
    title: "JavaScript Algorithms and Data Structures",
    issuerName: "freeCodeCamp",
    issuerImg: "freecodecamp.jpeg",
    issuedDate: new Date("2021-09-02"),
    url: "https://freecodecamp.org/certification/igorcmelo/javascript-algorithms-and-data-structures"
  },
  {
    title: "Advanced CSS and Sass: Flexbox, Grid, Animations and More!",
    issuerName: "Udemy",
    issuerImg: "udemy.jpeg",
    issuedDate: new Date("2021-06-02"),
    url: "https://www.udemy.com/certificate/UC-14aa4d9b-1232-46bf-a0c4-0545a2fb2cbb/"
  },
  {
    title: "Full Web Developer Course + 10 Projects",
    issuerName: "Udemy",
    issuerImg: "udemy.jpeg",
    issuedDate: new Date("2020-04-02"),
    url: "https://www.udemy.com/certificate/UC-1f48e892-bdb2-42d0-b139-38c00d1709fa/"
  },
]
</script>

<template>
  <div class="certificates-grid">
    <div class="certificate fx-col content-between" v-for="(cert, i) in certificates" :key="i">
      <div class="fx-row items-center g10">
        <img :src="cert.issuerImg" class="certificate__issuer-img" :title="cert.issuerName" />
        <div class="certificate__title">
          {{ cert.title }}
        </div>
      </div>
      <div class="fx-row content-between items-center">
        <div class="certificate__date">{{ formatDate(cert.issuedDate) }}</div>
        <a target="_blank" :href="cert.url" class="certificate__view fx-row items-center g10">
          <span>credential</span>
          <i class="fa fa-external-link"></i>
        </a>
      </div>
    </div>
  </div>
</template>

<style scoped lang="sass">

.certificates-grid
  display: grid
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr))
  gap: 15px

.certificate
  box-shadow: -1px 1px 5px #0004
  background-image: linear-gradient(45deg, hsl(0, 0, 95%), hsl(0, 0, 100%))
  padding: 15px
  gap: 20px

  &__title
    font-size: 18px

  &__date
    font-size: 15px

  &__issuer-img
    width: 40px
    height: 40px
    border-radius: 25%

  &__view
    color: #000c
    // color: white
    font-size: 15px
    padding: 7px 13px
    border: 2px solid #0007
    border-radius: 1000px
    text-align: center
    background-color: white
    // background-color: hsl(0, 0, 10%)
    // background-image: linear-gradient(to bottom, hsl(0, 0, 60%), hsl(0, 0, 50%))
</style>