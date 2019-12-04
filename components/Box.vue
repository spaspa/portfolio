<template lang="pug">
div.container
  a(:href="href")
    img(:src="src")
  p {{ description }}
</template>

<script>
export default {
  props: {
    src: String,
    href: String,
    description: String
  }
}
</script>

<style lang="sass" scoped>
@import "~/assets/main.scss"

.container
  width: 300px
  height: 450px
  display: flex
  align-items: center
  justify-content: space-between
  flex-direction: column
  background: white
  margin-bottom: 60px
  max-width: 300px
  > *
    max-width: 90%
  a
    margin: 1rem 1rem 0 1rem
  p
    color: #626262
    margin: 0 1rem 1rem 1rem

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
