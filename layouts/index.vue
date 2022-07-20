<template>
  <div>
    <div class="container">
      <div class="row">
        <div class="col-md-6 pb-4">
          <div class="w-100 mb-1 position-relative fixed-ratio">
            <div class="position-absolute">
              <img
                src="/browser-03.png"
                class="w-100"
                alt=""
              >
            </div>
          </div>
          <div class="pl-2">
            <span class="font-weight-bold text-light">
              DjaoDjin
            </span><br>
            <p class="mb-1">
              An integrated <em>SaaS</em> product offering full-service payment and account management features for small businesses.
            </p>
            <a href="/studies/">Case Study</a> | <a href="https://dd-dashboard.netlify.com">Prototype</a> | <a href="https://djaodjin.com">Homepage</a> | <a href="https://github.com/djaodjin/djaoapp">Github</a>
          </div>
        </div>
        <div class="col-md-6 pb-4">
          <div class="w-100 mb-1 position-relative fixed-ratio">
            <div class="position-absolute">
              <img
                src="/browser-02.png"
                class="w-100"
                alt=""
              >
            </div>
          </div>
          <div class="pl-2">
            <span class="font-weight-bold text-light">
              UN Survivor Application (and Dashboard)
            </span><br>
            <p class="mb-1">
              An application and dashboard service for individuals and families of those affected by the California Wildfires.
            </p>
            <a href="unsurvivor-oss">Prototype</a> | <a href="https://invis.io/5VTM181XKRW#/380637354_App-01">Invision 1</a>, <a href="https://projects.invisionapp.com/share/CRTM199K49Y#/screens">Invision 2</a> | <a href="https://github.com/vishalbakshi/CallForCode">Github</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  transition: 'fade',
  data() {
    return {};
  }
};
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
