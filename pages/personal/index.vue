<template>
  <div>
    <div class="container pt-2">
      <div class="row">
        <div class="col-md-12 text-center font-small">
          <span class="pr-3"><nuxt-link to="/personal">General</nuxt-link></span>
          <!-- <span class="pr-3"><nuxt-link to="/about">Other</nuxt-link></span> -->
          <span class="pr-3"><nuxt-link to="/personal/all">All</nuxt-link></span>
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
            I experimented with building working web scrapers through different channels of web developlement.
          </p>
          <a href="">Demo</a> | <a href="">Github</a>
        </div>
        <div class="col-md-6 pb-4">
          <span class="font-weight-bold text-light">
            xNews
          </span><br>
          <p class="mb-1">
            I built a personal, aggregate new viewer with a focus on minimalism and simple design. 
          </p>
          <a href="https://xnews.netlify.com">Demo</a> | <a href="https://github.com/jpoechill/vuefrontendrtalk_demo">Github</a>
        </div>
        <div class="col-md-6 pb-4">
          <span class="font-weight-bold text-light">
            Destiny 2 Data Exporter
          </span><br>
          <p class="mb-1">
            I built a tool for Destiny 2 (PS4) players that can export current player stats in .JSON format.
          </p>
          <a href="https://xcrucibleexporter.netlify.com">Demo</a> | <a href="https://github.com/jpoechill/xcrucibleexporter">Github</a>
        </div>
        <div class="col-md-6 pb-4">
          <span class="font-weight-bold text-light">
            Destiny 2 Gambit Tracker
          </span><br>
          <p class="mb-1">
            I built a tool for Destiny 2 (PS4) players that tracks a players current Gambit score for those going for the 'Reckoning' title.
          </p>
          <a href="https://xcurrgpgames.netlify.com">Demo</a> | <a href="https://github.com/jpoechill/xCurrGPGames">Github</a>
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
