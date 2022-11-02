<template>
  <div class="experiences">
    <div class="experience fx-row items-center g10">
      <div class="company fx-row items-center g10">
        <img src="/essia.png" alt="">
        Essia
      </div>
      -
      <div class="position">Full Stack Developer</div>
      <div class="period">(Nov 2021 - Currently)</div>
    </div>

    <div class="experience-details">
      <p>
        Essia is a virtual learning environment that has <b>250,000</b> students, almost <b>8,000</b> digital interactive books and <b>210</b> schools.
      <p>
      </p>
        Our challenge is to provide high <b>scalability</b> and good <b>performance</b> to handle thousands of requests per day and provide a good user experience.
      </p>

      <br>

      <p>Pin points:</p>
      <ul class="pin-points">
        <li>I develop web pages using <b>Vue.js</b>, <b>HTML</b>, <b>CSS</b>, <b>JavaScript</b></li>
        <li>I develop endpoints <b>Java + Spring</b>, querying data from <b>ElasticSearch</b> and <b>MySQL</b></li>
        <li>I develop a image and video optimization service using <b>Go</b>, <b>RabbitMQ</b> and <b>FFmpeg</b></li>
        <li>I investigate and fix <b>performance issues</b>, like slowness, <b>memory leaks</b>, <b>memory bloats</b> and others</li>
        <li>I make <b>test automation</b> using <b>Jest</b>, <b>JUnit</b> and <b>Postman</b>, besides teaching my colleages how to write unit tests</li>
        <li>I develop features and fixes for our mobile app using <b>Flutter</b>, <b>SQLite</b>, <b>Couchbase</b></li>
        <li>I develop features and fixes also for our desktop app using <b>Electron</b>, <b>Express</b></li>
      </ul>
    </div>
  </div>
</template>

<style scoped lang="sass">
.experiences
  // padding: 0 20px
.experience
  font-size: 22px
  padding: 10px 0
  .company
    font-weight: bold

    img
      width: 20px
  .position
    // font-style: italic

  .period
    color: hsl(0, 0, 30%)
// .experiences
.experience-details
  width: 100%

  .pin-points
    margin-left: 20px

    li + li
      margin-top: 15px

  > *
    width: 100%

  p
    margin: 8px 0

  b
    color: hsl(0, 0, 15%)
</style>