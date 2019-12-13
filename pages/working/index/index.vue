<template>
  <div>

    <div class="container">
      <div class="row">
        <div class="col-md-6 pb-4">
          <div class="w-100 mb-1 position-relative fixed-ratio">
            <div class="position-absolute">
              <img src="/browser-04.png" class="w-100" alt="">
            </div>
          </div>
          <div class="pl-2">
            <span class="font-weight-bold text-light">
              PPCS Restore
            </span><br>
            <p class="mb-1">
              PPCS Restore is a national, family-run, commercial building restoration company based in the Bay Area.
            </p>
            <a href="https://ppc-restore.com">Homepage</a> | <a href="https://github.com/jpoechill/ppcs">Github</a>
          </div>          
        </div>
        <div class="col-md-6 pb-4">
          <div class="w-100 mb-1 position-relative fixed-ratio">
            <div class="position-absolute">
              <img src="/browser-03.png" class="w-100" alt="">
            </div>
          </div>
          <div class="pl-2">
            <span class="font-weight-bold text-light">
              DjaoDjin
            </span><br>
            <p class="mb-1">
              An integrated <em>SaaS</em> product offering full-service payment and account management features for small businesses.
            </p>
            <nuxt-link to="/studies/">Case Study</nuxt-link> | <a href="https://dd-dashboard.netlify.com">Prototype</a> | <a href="https://djaodjin.com">Homepage</a> | <a href="https://github.com/djaodjin/djaoapp">Github</a>
          </div>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  data() {
    return {}
  },
  transition: 'fade'
}
</script>

<style scoped>
.text-light {
  color: #333 !important;
}

.fixed-ratio {
  width: 100%;
  padding-bottom: 63.78%;
}
</style>
