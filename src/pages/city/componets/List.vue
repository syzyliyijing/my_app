<template>
    <div class="list">

         <!--当前城市 -->
        <div class="area">
            <div class="title border-topbottom">当前城市</div>
            <div class="button-list">
                <div class="button-wrapper">
                    <div class="button">北京</div>
                </div>
            </div>
        </div>
        
        <!--热门城市 -->
         <div class="area">
            <div class="title border-topbottom">当前城市</div>
            <div class="button-list">
                <div class="button-wrapper">
                    <div class="button">北京</div>
                </div>
                <div class="button-wrapper">
                    <div class="button">北京</div>
                </div>
                <div class="button-wrapper">
                    <div class="button">北京</div>
                </div>
                <div class="button-wrapper">
                    <div class="button">北京</div>
                </div>
                <div class="button-wrapper">
                    <div class="button">北京</div>
                </div>
            </div>
        </div>

         <!--链接城市 -->
         <div class="area">
            <div class="title border-topbottom">A</div>
            <div class="item-list">
                <div class="item border-bottom">
                    阿拉善
                </div>
                <div class="item border-bottom">
                    阿拉善
                </div>
                <div class="item border-bottom">
                    阿拉善
                </div>
                <div class="item border-bottom">
                    阿拉善
                </div>
                <div class="item border-bottom">
                    阿拉善
                </div>                
            </div>

             <div class="title border-topbottom">B</div>
            <div class="item-list">
                <div class="item border-bottom">
                    北京
                </div>
                <div class="item border-bottom">
                    北京
                </div>
                <div class="item border-bottom">
                    北京
                </div>
                <div class="item border-bottom">
                    北京
                </div>
                <div class="item border-bottom">
                    北京
                </div>                
            </div>

             <div class="title border-topbottom">C</div>
            <div class="item-list">
                <div class="item border-bottom">
                    长沙
                </div>
                <div class="item border-bottom">
                    长沙
                </div>
                <div class="item border-bottom">
                    长沙
                </div>
                <div class="item border-bottom">
                    长沙
                </div>
                <div class="item border-bottom">
                    长沙
                </div>                
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CityList'
}
</script>

<style lang="stylus" scoped>
  @import '~@/assets/styles/varibles.styl'
  .border-topbottom
    &:before
      border-color: #ffffff
    &:after
      border-color: #cccccc
  .border-bottom
    &:after
      border-color: #cccccc
  .title
    line-height .44rem
    background #eeeeee
    padding-left .2rem
    color #666
    font-size .26rem
  .button-list
    overflow hidden
    padding .1rem .6rem .1rem .1rem
    .button-wrapper
      float left
      width 33.33%
      .button
        text-align center
        margin .1rem
        padding .1rem 0
        border .02rem solid #cccccc
        border-radius .08rem
  .item-list
    .item
      line-height .64rem
      padding-left .06rem
</style>