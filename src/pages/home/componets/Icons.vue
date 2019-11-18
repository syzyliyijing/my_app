<template>
    
    <div class="icons">
      
         <div class="icon">
            <div class="icon-img">
                <img class="icon-img-content" src="http://img1.qunarzz.com/piao/fusion/1611/54/ace00878a52d9702.png" alt="">
            </div>
            <p class="icons-desc">景点门票</p>
        </div>
         <div class="icon">
            <div class="icon-img">
                <img class="icon-img-content" src="http://img1.qunarzz.com/piao/fusion/1711/df/86cbcfc533330d02.png" alt="">
            </div>
            <p class="icons-desc">滑雪季</p>
        </div>
         <div class="icon">
            <div class="icon-img">
                <img class="icon-img-content" src="http://img1.qunarzz.com/piao/fusion/1710/a6/83f636bd75ae6302.png" alt="">
            </div>
            <p class="icons-desc">泡温泉</p>
        </div>
         <div class="icon">
            <div class="icon-img">
                <img class="icon-img-content" src="http://img1.qunarzz.com/piao/fusion/1611/35/2640cab202c41b02.png" alt="">
            </div>
            <p class="icons-desc">植物园</p>
        </div>
         <div class="icon">
            <div class="icon-img">
                <img class="icon-img-content" src="http://img1.qunarzz.com/piao/fusion/1611/d0/e09575e66f4aa402.png" alt="">
            </div>
            <p class="icons-desc">游乐园</p>
        </div>
         <div class="icon">
            <div class="icon-img">
                <img class="icon-img-content" src="http://img1.qunarzz.com/piao/fusion/1611/59/569d3c096e542502.png" alt="">
            </div>
            <p class="icons-desc">必游榜单</p>
        </div>
         <div class="icon">
            <div class="icon-img">
                <img class="icon-img-content" src="http://img1.qunarzz.com/piao/fusion/1611/17/4bd370f3eb1acd02.png" alt="">
            </div>
            <p class="icons-desc">演出</p>
        </div>
          <div class="icon">
            <div class="icon-img">
                <img class="icon-img-content" src="http://img1.qunarzz.com/piao/fusion/1611/7f/b1ea3c8c7fb6db02.png" alt="">
            </div>
            <p class="icons-desc">城市观光</p>
        </div>


    </div>

</template>

<script>
export default {
    name:'HomeIcons'
}
</script>

<style lang="stylus" scoped>
  .icons
    overflow hidden
    height 0
    padding-bottom 50%
    margin-top 1%
    .icon
      position relative
      overflow hidden
      float left
      width 15%
      height 0
      margin-left 5%
      margin-right 5%
      padding-bottom 25%
      .icon-img
        position absolute
        top 0
        left 0
        right 0
        bottom .44rem
        box-sizing border-box
        .icon-img-content
          display block
          margin 0 auto 
          width 100%
          margin-top 15%
      .icons-desc
        position absolute
        left 0
        right 0
        bottom 0
        height .44rem
        line-height .44rem
        text-align center
</style>