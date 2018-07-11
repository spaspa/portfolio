<template lang="pug">
section
  div.hero.is-bold.is-primary.is-head.is-medium
    div.tabs.is-centered
      ul
        li(:class="active === 0 ? 'is-active' : ''" )
          nuxt-link(to="/") Top
        li(:class="active === 1 ? 'is-active' : ''")
          nuxt-link(to="/work") Work
        li(:class="active === 2 ? 'is-active' : ''")
          nuxt-link(to="/about") About
</template>

<script>
export default {
  props: {
    active: Number,
  },
}
</script>

<style lang="sass">
li
  transition: all 0.3s ease
li:not(.is-active)
  color: rgba(255, 255, 255, 0.3)
li:hover
  color: rgba(255, 255, 255, 1.0)
</style>
