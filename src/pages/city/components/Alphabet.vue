<template>
  <ul class="list">
    <li class="item"
        v-for="item of letters"
        :key="item"
        :ref="item"
        @click="handleLetterClick"
        @touchstart="handleTouchStart"
        @touchmove="handleTouchMove"
        @touchend="handleTouchEnd"
    >
      {{ item }}
    </li>
  </ul>
</template>

<script>
export default {
  name: 'CityAlphabet',
  props: {
    cities: Object
  },
  data () {
    return {
      touchStatus: false // 标识位
    }
  },
  computed: {
    letters () {
      const letters = []
      for (let i in this.cities) {
        letters.push(i)
      }
      // console.log(letters)
      return letters
    }
  },
  methods: {
    handleLetterClick (e) {
      // console.log(e.target.innerText)
      this.$emit('change', e.target.innerText)
    },
    handleTouchStart () {
      this.touchStatus = true
    },
    handleTouchMove (e) {
      if (this.touchStatus) {
        const startY = this.$refs['A'][0].offsetTop
        // console.log(startY)
        const touchY = e.touches[0].clientY - 79 // 手指触摸高度减去top header search 高度
        // console.log(touchY)
        const index = Math.floor((touchY - startY) / 20) // 滑动位置 字母下标
        console.log(index)
        if (index >= 0 && index < this.letters.length) {
          this.$emit('change', this.letters[index])
          console.log(index)
        }
      };
    },
    handleTouchEnd () {
      this.touchStatus = false
    }
  }
}
</script>

<style lang="stylus" scoped>
@import "~styles/varibles.styl"
.list
  display: flex
  flex-direction column
  justify-content center
  position absolute
  top 1.58rem
  right 0
  bottom 0
  width .4rem
  /*background: red*/
  .item
    text-align center
    line-height .4rem
    color $bgColor
</style>
