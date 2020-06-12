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
              <img src="/browser-05.jpg" class="w-100" alt="">
            </div>
          </div>
          <div class="pl-2">
            <span class="font-weight-bold text-light">
              Mellana Café
            </span><br>
            <p class="mb-1">
              Mellana Café is a café located in South Berkeley/Northern Oakland, offering hand-made juices, gourmet sandwiches, and coffee.
            </p>
            <a href="https://mellanacafe.com">Homepage</a> | 
            <a href="https://instagram.com/mellanacafe">Instagram</a>
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
