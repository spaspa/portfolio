<template lang="pug">
  section
    TheHeader(:active="2")
    div.container
      div.about
        h2 about
        hr
      div.description
        h3 Name
        p spaspa
        small (spa, Eleven-Lines)
      div.description
        h3 Belonging
        p Tokyo Institute of Technology
      div.description
        h3 Skills
        p Web Front-end(Vue.js, React.js, TypeScript, ...)
        p Vector Graphics(Adobe Illustrator)
      div.description
        h3 Interest in
        p Type System, Design

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

h2
  font-weight: 600
  color: $primary

h3
  font-weight: 600

.about
  margin-top: -100px
  width: 100px

.description
  margin: 10px
</style>
