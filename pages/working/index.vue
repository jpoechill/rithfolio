<template>
  <div>
    <div class="container pt-2">
      <div class="row">
        <div class="col-md-12 text-center font-small">
          <span class="pr-3" v-for="(link, index) in links" :key="index">
            <nuxt-link :to="link.url" :class="{ active: link.active }" class="nounderline">{{ link.title }}</nuxt-link>
          </span>
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
    return {
      links: [
        {
          active: false,
          title: 'Active',
          url: '/working/active'
        },
        {
          active: false,
          title: 'Showcase',
          url: '/working'
        },
        {
          active: false,
          title: 'Recent',
          url: '/working/all'
        },
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

        if (self.$route.path.split('/')[2] === currLink.url.split('/')[2]) {
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
</style>
