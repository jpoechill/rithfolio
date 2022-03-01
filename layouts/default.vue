<template>
  <div>
    <div class="w-100 custom-gradient border-bottom">
      <div class="container">
        <div class="row">
          <div class="col-md-12 py-3"></div>
        </div>
      </div>
    </div>
    <div class="w-100 pb-0  sticky-top border-bottom" style="background-color: #FFF; box-shadow: 0 .5rem 1rem rgba(0,0,0,.01)!important;">
    <div class="container">
      <div class="row  sticky-top">
        <div class="col-md-5 bg-white py-3 border-left border-right text-center px-4">
            <span class="font-weight-bold">
              <nuxt-link to="/working">Po Rith</nuxt-link>
            </span> | 
            <span>
              JavaScript x Design
            </span>
        </div>
        <div class="col-md-5 py-3 px-3">
          <img src="/squiggle.svg" class="w-100" alt="">
        </div>
        <div class="col-md-2 bg-white py-3 border-left border-right text-center px-4">
            <span class="font-weight-bold">
              <nuxt-link to="/working">CV</nuxt-link>
            </span>
        </div>
        <!-- <div class="col-md-8 bg-dark text-right">
          <span class="bg-light px-5 py-3">
            <nuxt-link to="/">
            CV
            </nuxt-link>
          </span>
          <span class="pr-3" v-for="(link, index) in links" :key="index">
            <nuxt-link :to="link.url" class="nounderline text-nowrap" :class="{ active: link.active }">{{ link.title }}</nuxt-link>
          </span>
        </div> -->
      </div>
    </div>
    </div>

    <div class="w-100 pt-2" style="background-color: #FFF;">
      <nuxt/>
    </div>

    <div class="w-100 py-4 bg-white border-top">
      <div class="container">
        <!-- <div class="row">
          <div class="col-md-12 overflow-hidden">
            <div class="ticker-wrap">
              <div class="ticker">
                <div class="ticker__item">
                  <span class="col-md-3 mb-3" v-for="(stock, index) in prices" :key="index">
                    <img :src="stock.img" :alt="stock.name" class="mb-1 mr-2" style="height: 24px;"> ${{ numberWithCommas(stock.price) }} 
                    (<span v-if="stock.change >= 0" class="text-success">+{{ stock.change }}%</span><span v-if="stock.change < 0" class="text-danger">{{ stock.change }}% </span>)
                  </span>
                </div>
              </div>
            </div>
          </div>
        </div> -->
        <!-- <div class="row text-center">
          <div class="col-md-3 mb-3" v-for="(stock, index) in prices" :key="index">
            <img :src="stock.img" :alt="stock.name" class="mb-1 mr-2" style="height: 24px;"> ${{ numberWithCommas(stock.price) }} 
            (<span v-if="stock.change >= 0" class="text-success">+{{ stock.change }}%</span><span v-if="stock.change < 0" class="text-danger">{{ stock.change }}% </span>)
          </div>
        </div> -->
        <div class="row">
          <div class="col-md-6 py-2">
            <span class="text-muted">
              <small><em>
                Hashtags: #Algorithms, #JavaScript, #Design, #Vue.js, #HTML/CSS, #Git
              </em></small>
            </span>
          </div>
          <div class="col-md-6 text-right py-2">
            <!-- <em> -->
              <small class="text-muted">
                 Proudly made with <a href="https://github.com/vuejs/vue" target="_blank" class="vue-link">Vue.js</a>. © 2022
              </small>
            <!-- </em> -->
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import axios from 'Axios'

  export default {
    data () {
      return {
        prices: [
          {
            name: 'Apple',
            ticker: 'AAPL',
            change: 0,
            img: '/stocks/apple.png',
            price: 0,
          },
          {
            name: 'Facebook',
            ticker: 'FB',
            change: 0,
            img: '/stocks/facebook.png',
            price: 0,
          },
          {
            name: 'Google',
            ticker: 'GOOG',
            change: 0,
            img: '/stocks/google.png',
            price: 0,
          },
          {
            name: 'Netflix',
            ticker: 'NFLX',
            change: 0,
            img: '/stocks/netflix.png',
            price: 0,
          },
          // {
          //   name: 'Microsoft',
          //   ticker: 'MSFT',
          //   change: 0,
          //   img: '',
          //   price: 0,
          // },
          // {
          //   name: 'Snapchat',
          //   ticker: 'SNAP',
          //   change: 0,
          //   img: '/stocks/netflix.png',
          //   price: 0,
          // },
          // {
          //   name: 'Amazon',
          //   ticker: 'AMZN',
          //   change: 0,
          //   img: '/stocks/netflix.png',
          //   price: 0,
          // },
          // {
          //   name: 'Shopify',
          //   ticker: 'SHOP',
          //   change: 0,
          //   img: '/stocks/netflix.png',
          //   price: 0,
          // },
          // {
          //   name: 'Tesla',
          //   ticker: 'TSLA',
          //   change: 0,
          //   img: '/stocks/netflix.png',
          //   price: 0,
          // },
          // {
          //   name: 'Pinterest',
          //   ticker: 'PINS',
          //   change: 0,
          //   img: '/stocks/netflix.png',
          //   price: 0,
          // },
        ],
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
    mounted() {

      this.prices.forEach((stock) => {
        axios.get('https://cloud.iexapis.com/stable/stock/' + stock.ticker + '/quote?token=pk_d8826aae332a4b1287b1d4399e2f860b')
        .then(function (response) { 
          // console.log(i + ': ' + response.data.high)

          stock.price = response.data.latestPrice
          stock.change = Math.floor(response.data.changePercent * 100) / 100
          })
        .catch(function (error) {
          console.log(error);
        })
      })
    },
    methods: {
      numberWithCommas: function(x) {
        return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
      },
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
  font-size: 16px;
  height: 100%;
  /* font-family: Arial, Helvetica, sans-serif; */
}

body {
  color: #333;
  background-color: #f7f7f7!important;
}

.vue-link {
  color: teal;
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

@-webkit-keyframes ticker {
  0% {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    visibility: visible;
  }
  100% {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
  }
}
@keyframes ticker {
  0% {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    visibility: visible;
  }
  100% {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
  }
}

.ticker-wrap {
  /* position: fixed; */
  /* bottom: 0; */
  width: 100%;
  overflow: hidden;
  /* height: 4rem; */
  /* background-color: rgba(0, 0, 0, 0.9); */
  padding-left: 100%;
  box-sizing: content-box;
}

.ticker-wrap .ticker {
  display: inline-block;
  height: 4rem;
  line-height: 4rem;
  white-space: nowrap;
  padding-right: 100%;
  box-sizing: content-box;
  -webkit-animation-iteration-count: infinite;
  animation-iteration-count: infinite;
  -webkit-animation-timing-function: linear;
  animation-timing-function: linear;
  -webkit-animation-name: ticker;
  animation-name: ticker;
  -webkit-animation-duration: 30s;
  animation-duration: 30s;
}
.ticker-wrap .ticker__item {
  display: inline-block;
  padding: 0 2rem;
  /* font-size: 2rem; */
  /* color: white; */
}
@media only screen and (max-width: 600px) {
  .text-responsive {
    text-align: center!important;
  }
}


</style>