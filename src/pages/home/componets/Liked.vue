<template>
    <div>
        <div class="title">
            <img src="http://img1.qunarzz.com/piao/fusion/1711/89/ebc329f16c55bb02.png" alt="" class="title-img">
            <span class="title-content">猜你喜欢</span>
        </div>
        <ul>
            <li class="item" v-for="item of likeList" :key="item.id">
                <img :src="item.imgUrl" alt="" class="item-img">
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p>
                        <span class="iconfont" v-html="item.star">{{item.star}}</span>
                        <span class="item-comment">{{item.comment}}</span>
                    </p>
                    <p class="item-price"><em>￥</em>{{item.price}}<span>起</span></p>
                    <p class="item-desc">{{item.desc}}</p>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name:'HomeLiked',
    data () {
        return{
            likeList:[{
                      id: '001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_200x200_2039e660.jpg',
        title: '上海迪士尼乐园',
        star:'&#xe627;&#xe627;&#xe627;&#xe627;&#xe627;&#xe627;',
        comment:'277442条评论',
        price: '394',
        desc: '全球最大的迪士尼城堡'
      }, {
        id: '002',
        imgUrl: 'http://img1.qunarzz.com/tuan/team2/1507/2c/83e0e0e7ae082a.jpg_200x200_6d7378b2.jpg',
        title: '东方明珠',
        star:'&#xe627;&#xe627;&#xe627;&#xe627;',
        comment:'87877条评论',
        price: '80',
        desc: '259米透明悬空观光廊了解一下~'
      }, {
        id: '003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1906/19/19b7939928a0200da3.img.jpg_200x200_6879c7f7.jpg',
        title: '上海海昌海洋公园',
        star:'&#xe627;&#xe627;&#xe627;&#xe627;&#xe627;',
        comment:'25826条评论',
        price: '139',
        desc: '全球最大的迪士尼城堡'
      }, {
        id: '004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1803/26/2645c1b2ee526285a3.water.jpg_250x250_c9ab8185.jpg',
        title: '上海迪士尼乐园',
        star:'&#xe627;&#xe627;&#xe627;',
        comment:'277442条评论',
        price: '394',
        desc: '全球最大的迪士尼城堡'
      },  {
        id: '005',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1811/e4/e4b9b471d2afc473a3.img.jpg_250x250_963fe222.jpg',
        title: '东方明珠',
        star:'&#xe627;&#xe627;&#xe627;&#xe627;',
        comment:'87877条评论',
        price: '80',
        desc: '259米透明悬空观光廊了解一下~'
      }]
        }
    }
}
</script>

<style lang="stylus" scoped>
  .title
    margin-top .2rem
    background #eeeeee
    padding .2rem
    text-align left 
    .title-img
      width .3rem
      height .3rem
      margin-top -.09rem
    .title-content
      margin-left .08rem
      height .44rem
      color red
      font-size .32rem
      line-height .44rem
  .item
    overflow hidden
    display flex
    height 1.9rem
    padding-bottom 1rem
    border-bottom 1px solid #cccccc
    .item-img
      width 2.3rem
      height 2.3rem
      padding .2rem
    .item-info
      flex 1
      padding .1rem
      margin-top .3rem
      min-width 0
      .item-title
        height .44rem
        color #212121
        font-size .32rem
        line-height .44rem
        margin-bottom .1rem
      .iconfont
        color #ffb436
        font-size .25rem
      .item-comment
        color #212121
        margin-left .2rem
      .item-price
        font-size .4rem
        color #ffb436
        margin-top .2rem
        em
          font-size .25rem
        span 
          color #616161
          font-size .25rem
      .item-desc
        margin-top .6rem
        color #ff5555
        font-size .24rem  
</style>