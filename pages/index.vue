<template>
  <div>
    <div class="container pt-2">
      <div class="row">
        <div class="col-md-12 text-center font-small">
          <span class="pr-3"><nuxt-link to="/active">Active</nuxt-link></span>
          <span class="pr-3"><nuxt-link to="/">Showcase</nuxt-link></span>
          <span class="pr-3"><nuxt-link to="/all">Recent</nuxt-link></span>
        </div>
        <div class="col-md-12">
          <hr>
        </div>
      </div>
    </div>

    <NuxtChild/>

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

<style>
</style>
