<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{this.city}}
        <span class="iconfont arrow-icon">&#xe64a;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
  .header
    display : flex
    /*height : 0.86rem*/
    line-height $headerHeight
    background $bgColor
    color #ffffff
    .header-left
      width : 0.64rem
      float : left
      .back-icon
        text-align center
        font-size .4rem
    .header-input
      flex : 1
      margin-top .12rem
      margin-left .2rem
      padding-left .2rem
      height .64rem
      background #ffffff
      border-radius : .1rem
      color #cacaca
      line-height .64rem
    .header-right
      width : 1.24rem
      float : right
      text-align center
      color #ffffff
      .arrow-icon
        font-size .24rem
        margin-left -.04rem
</style>
