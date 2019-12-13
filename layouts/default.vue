<template>
  <div>
    <div class="w-100 custom-gradient">
      <div class="container">
        <div class="row">
          <div class="col-md-12 py-3"></div>
        </div>
      </div>
    </div>
    <div class="w-100 pb-3" style="background-color: #F7F7F7;">
    <div class="container">
      <div class="row pt-3">
        <div class="col-md-4 pb-2 text-responsive">
            <span class="font-weight-bold">
              <nuxt-link to="/working">Po Rith</nuxt-link>
            </span> | 
            <span>
              Design x Javascript (Vue.js)
            </span>
        </div>
        <div class="col-md-8 text-right text-responsive">
          <span class="pr-3" v-for="(link, index) in links" :key="index">
            <nuxt-link :to="link.url" class="nounderline text-nowrap" :class="{ active: link.active }">{{ link.title }}</nuxt-link>
          </span>
        </div>
      </div>
    </div>
    </div>

    <div class="w-100 pt-2 pb-4" style="background-color: #FFF;">
      <nuxt/>
    </div>

    <div class="w-100 py-4">
      <div class="container">
        <div class="row text-center">
          <div class="col-md-12">
            🐴 🦄 Rithfolio.com © 2019
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
        links: [
          {
            active: false,
            title: 'About',
            url: '/about'
          },
          {
            active: false,
            title: 'Working Projects',
            url: '/working'
          },
          {
            active: false,
            title: 'Personal Projects',
            url: '/personal'
          },
          {
            active: false,
            title: 'Contact',
            url: '/contact'
          }
        ],
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
    created() {
      this.checkLinks()
    },
    methods: {
      checkLinks: function () {
        let self = this

        this.links = this.links.map(function (link) {
          // update schema if page route matches link url

          let currLink = link

          if (self.$route.path.split('/')[1] === currLink.url.split('/')[1]) {
            currLink.active = true
          } else {
            currLink.active = false
          }

          return link
        })
      }
    },
    watch:{
      $route (to, from){
        this.checkLinks()
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
  background-color: #f7f7f7!important;
}

.custom-gradient {
  background: linear-gradient(215deg, #ff0000, #feff00, #6bff00, #00ffe6, #0100ff, #cc00ff, #ff0000);
  background-size: 1400% 1400%;

  -webkit-animation: AnimationName 120s ease infinite;
  -moz-animation: AnimationName 120s ease infinite;
  animation: AnimationName 120s ease infinite;
}
@-webkit-keyframes AnimationName {
    0%{background-position:0% 51%}
    50%{background-position:100% 50%}
    100%{background-position:0% 51%}
}
@-moz-keyframes AnimationName {
    0%{background-position:0% 51%}
    50%{background-position:100% 50%}
    100%{background-position:0% 51%}
}
@keyframes AnimationName {
    0%{background-position:0% 51%}
    50%{background-position:100% 50%}
    100%{background-position:0% 51%}
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

.active {
  padding-bottom: 2px;
  border-bottom: 3px solid #ddd;
}

.nounderline {
  text-decoration: none !important
}

@media only screen and (max-width: 600px) {
  .text-responsive {
    text-align: center!important;
  }
}
</style>