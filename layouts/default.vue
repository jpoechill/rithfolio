<template>
  <div>
    <div class="w-100" style="background-color: #4A90E2;">
      <div class="container">
        <div class="row">
          <div class="col-md-12 py-3"></div>
        </div>
      </div>
    </div>

    
    <div class="w-100 pb-3" style="background-color: #F7F7F7;">
    <div class="container">
      <div class="row pt-3">
        <div class="col-md-4 text-responsive">
            <span class="font-weight-bold">
              <nuxt-link to="/">Po Rith</nuxt-link>
            </span> | 
            <span>
              Design x Javascript (Vue.js)
            </span>
        </div>
        <div class="col-md-8 text-right text-responsive">
          <span class="pr-3"><nuxt-link to="/about">About</nuxt-link></span>
          <span class="pr-3"><nuxt-link to="/">Working Projects</nuxt-link></span>
          <span class="pr-3"><nuxt-link to="/personal">Personal Projects</nuxt-link></span>
          <span class="pr-3"><nuxt-link to="/contact">Contact</nuxt-link></span>
        </div>
      </div>
    </div>
    </div>

    <div class="w-100 pt-2 pb-5" style="background-color: #FFF;">
      <nuxt/>
    </div>

    <div class="w-100 py-4">
      <div class="container">
        <div class="row text-center text-white">
          <div class="col-md-12">
            Rithfolio.com © 2019 
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        title: 'Po Rith | Rithfolio.com'
      }
    },
    head () {
      return {
        title: this.title,
        meta: [
          { hid: 'Po Rith | Rithfolio.com', name: 'Po Rith | Rithfolio.com', content: 'Po Rith is a designer and vue.js developer from Oakland, CA.' }
        ]
      }
    },
    transition: 'fade'
  }
</script>

<style>
body, html {
  font-size: 18px;
  height: 100%;
}

body {
  color: #333;
  background-color: #333!important;
}

.fade-enter-active, .fade-leave-active {
  transition: opacity .2s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}

.logo {
  min-width: 150px;
}

.special {
  font-size: 22px;
}

.weight-400 {
  font-weight: 400;
}

.weight-600 {
  font-weight: 600;
}

@media only screen and (max-width: 600px) {
  .text-responsive {
    text-align: center!important;
  }
}
</style>