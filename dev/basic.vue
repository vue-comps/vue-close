<template lang="jade">
.container
  a(href="https://github.com/vue-comps/vue-parallax/blob/master/dev/basic.vue") source
  close
  close(disabled) disabled
  span {{state}}
</template>

<script lang="coffee">
module.exports =
  data: -> state:""
  components:
    "close": require "../src/close.vue"
  events:
    close: ->
      @state="received close"
      @clearTimeout?()
      @clearTimeout = setTimeout (=>@state=""),2000
      true
</script>

<style lang="stylus">
.container > a
  position absolute
  left 250px
  top 40px
</style>
