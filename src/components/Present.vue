<template>
  <div class="main">
    <div class="containerC" id="containerC">
      <div class="content" id="content">
        <!-- <el-button @click="scrollToBottom()">test</el-button> -->
        <!-- artwork4 -->
        <div class="artwork" id="art4">
          <div id="music">
            <iframe id="musicplayer" src="https://rever-artwork4.glitch.me/" frameborder="0"></iframe>
          </div>
          <div class="art-title">Sinestesia</div>
          <div class="description">How are you feeling right now? Are you anxious? Excited? Maybe a bit of both?<br>Sometimes it’s hard to convey to others exactly how we feel and whats in our minds,<br>but visualization of our emotions might help give a more defined shape to abstracts<br> features and help us express them to others.</div>
        </div>
        <!-- welcome -->
        <div id="welcome">
          <div class="sub-title">Welcome to the present</div>
          <div class="text">The present is nothing but a punctual, specific moment in time,<br>everflowing from the uncertainty of the future yet to come to the<br>solidty of the past already gone.<br>The experiences you make here are momentary and soon become<br>elements quickly disappearing in front of your eyes. </div>
        </div>
      </div>
    </div>
    <iframe id="bg" src="/bg_present.html" frameborder="0" width="100vw" height="100vh" scrolling="auto"></iframe>
  </div>
</template>

<script>
export default {
  methods: {
    scrollToBottom() {
      var content = this.$el.querySelector('#containerC')
      content.scrollTop = content.scrollHeight
      // console.log(content.scrollHeight)
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import url('../style.css')

  .main
    background-color white
    display relative
    align-items center
  .art-title,
  .description,
  .sub-title,
  .text
    color black

  #art4
    margin-top 15vh

  #music-bg
    height 50vh
    background-image url('../assets/music.png')
    background-size: contain;
    background-position center
    background-repeat: no-repeat;
    margin-bottom 8vh

  .button
    margin 5vh 0 0 0

  #musicplayer
    width 48vw
    height 65vh
    border-radius 10px
    filter drop-shadow(3px 3px 20px rgba(169,140,219,0.4))

  #welcome
    margin 60vh 0 45vh 0

  .main
    height 100vh
  .containerC
    height 100%
    overflow auto
    position relative
  .content
    position relative
    z-index 2
    bottom 0
  #bg
    height 100vh
    position absolute
    bottom 0
    left 0
    z-index 1
</style>
