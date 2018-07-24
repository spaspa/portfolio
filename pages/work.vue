<template lang="pug">
  section
    TheHeader(:active="1")
    div.container
      Box(src="/work/otakublocker.png"
          href="https://otakublocker.spaspa.me")
      Box(src="/work/prism.png")
      Box(src="/work/prism_poster.png")
      Box(src="/work/palette.png")
</template>

<script>
import TheHeader from '~/components/TheHeader.vue'
import Box from '~/components/Box.vue'

export default {
  components: {
    TheHeader,
    Box
  }
}
</script>

<style lang="sass" scoped>
.container
  display: flex
  align-items: center
  justify-content: center
  flex-direction: row
  flex-wrap: wrap
  margin-top: 60px
  width: 100vw
</style>
