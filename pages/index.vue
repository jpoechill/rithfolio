<template>
  <div></div>
</template>

<script>
export default {
  data() {
    return {}
  },
  created() {
    this.$router.push({
        path: '/working'
    })
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
