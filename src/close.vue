// out: ..
<template lang="jade">
button(@click="close | notPrevented | prevent")
  slot Close
</template>

<script lang="coffee">
module.exports =

  filters:
     notPrevented: require("vue-filters/notPrevented")
     prevent: require("vue-filters/prevent")

  methods:
    close: ->
      @$emit("beforeClose")
      @$dispatch("close")
</script>
