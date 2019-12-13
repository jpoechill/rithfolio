<template>
  <div>
    <div class="container pt-2">
      <div class="row">
        <div class="col-md-12 text-center font-small">
          <span class="pr-3"><nuxt-link to="/personal" class="active nounderline">Most Recent</nuxt-link></span>
          <!-- <span class="pr-3"><nuxt-link to="/personal/all" class="nounderline">Everything</nuxt-link></span> -->
        </div>
        <div class="col-md-12">
          <hr>
        </div>
      </div>
    </div>


    <div class="container pt-4">
      <div class="row">
        <div class="col-md-6 pb-4">
          <span class="font-weight-bold text-light">
            Web Scrapers
          </span><br>
          <p class="mb-1">
            An experiment in building working web scrapers through different channels of serverless web developlement.
          </p>
          <a href="https://loving-mayer-d80a26.netlify.com/.netlify/functions/dboom-mostrecent">Demo 1</a>, <a href="https://loving-mayer-d80a26.netlify.com/.netlify/functions/dboom-highlights">Demo 2</a> | <a href="https://github.com/jpoechill/netlifyfunctions-helloworld/">Github</a>
        </div>
        <div class="col-md-6 pb-4">
          <span class="font-weight-bold text-light">
            xNews
          </span><br>
          <p class="mb-1">
            A personal, aggregate news viewer with a focus on minimalism and simple design. 
          </p>
          <a href="https://xnews.netlify.com">Demo</a> | <a href="https://github.com/jpoechill/vuefrontendrtalk_demo">Github</a>
        </div>
        <div class="col-md-6 pb-4">
          <span class="font-weight-bold text-light">
            Destiny 2 Data Exporter
          </span><br>
          <p class="mb-1">
            A tool for Destiny 2 (PS4) players that can export current player stats in .JSON format.
          </p>
          <a href="https://xcrucibleexporter.netlify.com">Demo</a> | <a href="https://github.com/jpoechill/xcrucibleexporter">Github</a>
        </div>
        <div class="col-md-6 pb-4">
          <span class="font-weight-bold text-light">
            Destiny 2 Gambit Tracker
          </span><br>
          <p class="mb-1">
            A tool for Destiny 2 (PS4) players that tracks a players current Gambit score for those going for the 'Reckoning' title.
          </p>
          <a href="https://xinfamous.tk">Demo</a> | <a href="https://github.com/jpoechill/xinfamous">Github</a>
        </div>
        <div class="col-md-6 pb-4">
          <span class="font-weight-bold text-light">
            Pinterest Clone
          </span><br>
          <p class="mb-1">
            A simple Pinterest clone made with Vue.js, Bootstrap, and Firebase's Serverless DB.
          </p>
          <a href="">Demo</a> | <a href="https://github.com/jpoechill/pinterestclone">Github</a>
        </div>
        <div class="col-md-6 pb-4">
          <span class="font-weight-bold text-light">
            Vue, Stripe Payments
          </span><br>
          <p class="mb-1">
            A simple serverless application that tests abilities to make Stripe payments sans a proper backend.
          </p>
          <a href="">Demo</a> | <a href="">Github</a>
        </div>
      </div>
    </div>

    <div class="container">
      <div class="row">
        <div class="col-md-12 text-center mx-2 my-2 text-white py-2 text-uppercase weight-bold" style="background-color: #007AFF; font-weight: 600; letter-spacing: 1.5px; cursor: pointer;">
          More Projects
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
    }
  },
  transition: 'fade'
}
</script>

<style scoped>
.text-light {
  color: #333 !important;
}
</style>
