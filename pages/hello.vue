<template>
  <div>
    <div class="position-relative">
      <div class="w-100 position-fixed d-none d-lg-block z-index-back vh-100 overflow-hidden">
        <img src="/portrait.jpg" class="portrait h-100" alt="">
      </div>
      <!-- <div class="w-100 position-fixed d-lg-none z-index-back overflow-hidden">
        <img src="/portrait-centered.jpg" class="portrait w-100 h-100" alt="">
      </div> -->
      <!-- Visible on Mobile -->
      <div class="container pt-0">
        <div class="row pt-5">
          <div class="offset-md-3 pt-4 pr-4 pb-3 col-md-9 bg-light">
            <div class="pl-3">
              <div class="row">
                <div class="col-md-6">
                  <h3>Po Rith</h3>
                  <h5 class="pb-0"><i>Design + Vue.js Development</i></h5>
                  heys@rithfolio.com 
                  <br><br>
                </div>
                <div class="col-md-6 text-right">
                  <img src="/social/twitter.png" class="logo-social" alt="Twitter Logo">
                  <img src="/social/github.png" class="logo-social" alt="Github Logo">
                  <img src="/social/medium.png" class="logo-social" alt="Medium Logo">
                  <img src="/social/dribbble.png" class="logo-social" alt="Dribbble Logo">
                  <img src="/social/linkedin.png" class="logo-social" alt="LinkedIn Logo">
                </div>
              </div>
              <div class="row">
                <div class="col-md-12">
                  <nuxt-link to="/hello/">Working Projects</nuxt-link> | 
                  <nuxt-link to="/hello/personal">Personal Projects</nuxt-link> | 
                  <nuxt-link to="/hello/other">Other Projects</nuxt-link> 
                  <!-- <nuxt-link to="/hello/contact">Contact</nuxt-link> -->
                </div>
              </div>
              <nuxt-child />
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- <div class="container position-relative">
      <div class="position-absolute z-index-back">
        <img src="/portrait.png" alt="">
      </div>
      <div class="d-none d-lg-block">
        <div class="row">
          1231 <br> asdas
        </div>
      </div>
    </div> -->
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  },
  data() {
    return {
      emailText: "Email"
    }
  },
  methods: {
    handleToggle () {
      this.emailText = 'heys@rithfolio.com'
    }
  },
}
</script>

<style scoped>
body, html {
  font-size: 18px;
  height: 100%;
}

.mh-special {
  min-height: 440px;
}

.logo {
  min-width: 150px;
}

.logo-social {
  width: 24px;
  height: 24px;
}

.portrait {
  min-height: 500px;
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

.z-index-back {
  z-index: -1000;
}
</style>
