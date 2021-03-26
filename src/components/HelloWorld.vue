<template>
  <div class="hello">
    <div class="md-wrapper" v-html="html" ref="html"></div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    html: String
  },
  mounted () {
  },
  watch: {
    html: function () {
      const template = this.$refs.html
      this.$nextTick(() => {
        const p = template.querySelector('.markdown-body p')
        console.log(p)
      })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
