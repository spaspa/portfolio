<template lang="pug">
  section.hero
    TheHeader(:active="0")
    div.container
      h1 Portfolio
      div.links
        router-link.link-item(to="/work") work
        router-link.link-item(to="/about") about
</template>

<script>
import TheHeader from '~/components/TheHeader.vue'

export default {
  components: {
    TheHeader
  }
}
</script>

<style lang="sass" scoped>
@import "@/assets/main.scss"

.container
  height: calc(100vh - 60px)
  padding-top: 20px
  text-align: center
  display: flex
  align-items: center
  justify-content: center
  flex-direction: column

h1
  font-size: 40pt
  margin-bottom: 40px

.links
  width: 300px
  display: flex
  align-items: center
  justify-content: space-around

.link-item
  font-size: 20pt
  &:before, &:after
    content: ""
    position: absolute
    width: 40px
    height: 40px
    border-color: $primary
    border-style: solid
    border-width: 0

    &:before
      left: 0
      bottom: 0
      border-bottom-width: 1px
      border-left-width: 1px
    &:after
      top: 0
      right: 0
      border-top-width: 1px
      border-right-width: 1px

  &:hover
    &:before, &:after
      transition: all 2s cubic-bezier(.14,1.13,0,.91)
      opacity: 1
    &:before
      transform: translate(-35px, 15px) scale(1)
      border-bottom-width: 5px
      border-left-width: 5px
    &:after
      transform: translate(5px, -15px) scale(1)
      border-top-width: 5px
      border-right-width: 5px
</style>
