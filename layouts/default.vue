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
</style>
