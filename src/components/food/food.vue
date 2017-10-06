<template>
  <div v-show="showFlag" class="food">
    <div class="food-content">
      <div class="image-header">
        <img :src="food.image">
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      food: {
        type: Object
      }
    },
    data () {
      return {
        showFlag: false
      }
    },
    methods: {
      show () {
        this.showFlag = true
      }
    }
  }
</script>

<style lang="stylus" rel="stylesheet/stylus">
  .food
    position fixed
    left 0
    top 0
    bottom 48px
    z-index 30
    width 100%
    background: #fff

</style>
