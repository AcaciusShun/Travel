<template>
  <div class="header">
    <div class="header-left">返回</div>
    <div class="header-input">输入城市游玩主题</div>
    <div class="header-right">城市</div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  .header
    display : flex
    /*height : 0.86rem*/
    line-height .86rem
    background #25a4bb
    color #ffffff
    .header-left
      width : 0.64rem
      float : left
    .header-input
      flex : 1
      margin-top .12rem
      margin-left .2rem
      height .64rem
      background #ffffff
      border-radius : .1rem
      color #cacaca
      line-height .64rem
    .header-right
      width : 1.24rem
      float : right
      text-align center
</style>
