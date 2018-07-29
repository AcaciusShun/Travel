<template>
<div class="icons">
  <div class="icon">
    <div class="icon-img">
      <img class="icon-img-content" src="http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png" alt="">
    </div>
    <p class="icon-desc">热门景点</p>
  </div>
</div>
</template>
<script>
export default {

}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .icons
    overflow: hidden
    width 100%
    height 0
    padding-bottom 50%
    /*background: #010133*/
    .icon
      position relative
      overflow hidden
      float left
      width 25%
      height 0
      padding-bottom 25%
      /*background #25a4bb*/
      .icon-img
        position: absolute
        top 0
        left 0
        right 0
        bottom .44rem
        box-sizing border-box
        padding .1rem
        /*background: #cacaca*/
        .icon-img-content
          display block
          margin 0 auto
          height 100%
      .icon-desc
        position: absolute
        left 0
        right 0
        bottom 0
        height .44rem
        line-height .44rem
        color $darkTextColor
        text-align center
</style>
