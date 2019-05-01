<template>
  <div>
    <div class="container d-flex align-items-center justify-contents-center pt-5">
      <div class="d-none d-lg-block">
        <div class="row">
          <div class="offset-md-2 col-md-3 text-right">
            <img src="logo-xl.png" class="logo w-75" alt=""> <br>
            <!-- mb-3 pt-2 pr-2 pl-5 -->
          </div>
          <div class="col-md-4">
            <h5></h5>
              <span class="weight-600 special">Po Rith</span>
              <p>
                <span class="weight-400"><i>design + vue.js development</i></span>
              </p>
              <p>
                currently working on: <br>
                <a href="https://portraitsdaily.com">portraitsdaily.com</a>
              </p>
              <p>
                heys@rithfolio.com<br>
                <a href="https:/medium.com/rithfolio">Medium</a> | <a href="https://github.com/jpoechill">Github</a> | <a href="https://dribbble.com/jpoechill">Dribbble</a>
              </p>
            <br><br>
          </div>
        </div>
      </div>
      <div class="d-none d-md-block d-lg-none ">
        <div class="row">
          <div class="offset-md-2 col-md-3 text-right">
            <img src="logo-xl.png" class="logo w-50" alt=""> <br>
          </div>
          <div class="col-md-5">
            <h5></h5>
              <span class="weight-600 special">Po Rith</span>
              <p>
                <span class="weight-400"><i>design + vue.js development</i></span>
              </p>
              <p>
                currently working on: <br>
                <a href="https://portraitsdaily.com">portraitsdaily.com</a>
              </p>
              <p>
                heys@rithfolio.com<br>
                <a href="https:/medium.com/rithfolio">Medium</a> | <a href="https://github.com/jpoechill">Github</a> | <a href="https://dribbble.com/jpoechill">Dribbble</a>
              </p>
            <br><br>
          </div>
        </div>
      </div>
      <div class="d-lg-none d-md-none">
        <div class="row">
          <div class="offset-md-2 col-md-3 text-center">
            <img src="logo-xl.png" class="w-25 logo" alt=""> <br>
          </div>
          <div class="col-md-4 text-center pt-4">
            <h5></h5>
              <span class="weight-600 special">Po Rith</span>
              <p>
                <span class="weight-400"><i>design + vue.js development</i></span>
              </p>
              <p>
                currently working on: <br>
                <a href="https://portraitsdaily.com">portraitsdaily.com</a>
              </p>
              <p>
                heys@rithfolio.com<br>
                <a href="https:/medium.com/rithfolio">Medium</a> | <a href="https://github.com/jpoechill">Github</a> | <a href="https://dribbble.com/jpoechill">Dribbble</a>
              </p>
            <br><br>
          </div>
        </div>
      </div>
    </div>
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

<style>
body, html {
  font-size: 18px;
  height: 100%;
}

.container {
  min-height: 100vh;
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
</style>
