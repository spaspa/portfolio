<template lang="pug">
  section
    TheHeader(:active="1")
    .work-container
      .containers
        Box(src="/work/traQ.png"
            href="https://trap.jp/post/886/"
            description="traQ: 開発参加")
        Box(src="/work/tsundoku.png"
            href="https://tsun-doku.app"
            description="ツンドク: 開発参加")
        Box(src="/work/frontier.png"
            href="https://2018.koudaisai.jp/"
            description="工大祭2018パンフレット表紙")
        Box(src="/work/prism.png"
            href="https://2017.koudaisai.jp/"
            description="工大祭2017パンフレット表紙")
        Box(src="/work/prism_poster.png"
            href="https://2017.koudaisai.jp/"
            description="工大祭2017ポスター")
        Box(src="/work/palette.png"
            href="https://2016.koudaisai.jp/"
            description="工大祭2016パンフレット表紙")
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
.work-container
  width: 100%
  display: flex
  align-items: center
  justify-content: center
.containers
  display: flex
  align-items: center
  justify-content: center
  flex-direction: row
  flex-wrap: wrap
  margin-top: 60px
  width: 100vw
  max-width: 1000px
</style>
