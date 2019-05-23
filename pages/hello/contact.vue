<template>
  <div>
    <div class="row pt-2">
      <div class="col-md-12">
        Email: heys@rithfolio.com <br><br>
        Github | Dribbble | Medium | LinkedIn
        <br><br><br><br><br><br><br><br><br>
        <!-- Github: https://myurl.com <br>
        Dribbble: https://myurl.com <br>
        Medium: https://myurl.com <br>
        LinkedIn: https://myurl.com <br> -->
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
