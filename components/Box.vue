<template lang="pug">
div.container
  a(:href="href")
    img(:src="src")
</template>

<script>
export default {
  props: {
    src: String,
    href: String
  }
}
</script>

<style lang="sass" scoped>
@import "~/assets/main.scss"

.container
  width: 300px
  height: 400px
  display: flex
  align-items: center
  justify-content: center
  flex-direction: column
  background: white
  margin-bottom: 60px
  > *
    max-width: 90%

.container:after
  content: ""
  position: absolute
  z-index: -1
  height: 100%
  width: 100%
  transform: translateX(2px) translateY(2px)
  opacity: 0.3
  background: linear-gradient(to right, $primary, $success)
  filter: blur(3px)
  transition: all 0.2s

</style>
