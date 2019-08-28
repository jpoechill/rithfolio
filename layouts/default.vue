<template>
  <div>
    <nuxt />
  </div>
</template>

<script>
export default {
  data () {
    return {
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
  }
}
</script>

<style>
body {
  color: #333;
  background-color: #333!important;
}

.fade-enter-active, .fade-leave-active {
  transition: opacity .2s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
