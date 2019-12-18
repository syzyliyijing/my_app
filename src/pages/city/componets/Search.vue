<template>
<div>
    <div class="search">
        <input v-model="keyword"
                type="text" 
                class="search-input" 
                placeholder="输入城市名或拼音">

    </div>
    <div class="search-content"
         ref="search"
         v-show="keyword">
      <ul>
        <li
            v-for="item of list"
            :key="item.id"
            class="search-item border-bottom">{{item.name}}</li>
        <li class="search-item border-bottom"
            v-show="hasNoData">未找到匹配的数据</li>
      </ul>
    </div>
</div>
</template>

<script>
import Bscroll from "better-scroll"
export default {
    name: 'CitySearch',
    props:{
      cities:Object
    },
    //在data里初始化Keyword，list，timer
    //keyword是我们搜索的关键字
    //list是搜索之后的结果数据
    //timer是一个提高搜索性能的计时器
    data (){
      return{
        keyword:'',
        list:[],
        timer:null
      }
    },
    //通过取反是否有数据
    computed:{
      hasNoData (){
        console.log(!this.list.length)
        return !this.list.length
      }
    },
    //添加watch监听keyword函数
    watch:{
      keyword (){
        if(this.timer){
          clearTimeout(this.timer)
        }
        if(!this.keyword){
          this.list=[]
          return
        }
        this.timer = setTimeout( () =>{
          const result = []
          for (let i in this.cities){
            this.cities[i].forEach((value)=>{
              if (value.spell.indexOf(this.keyword) > -1
                || value.name.indexOf(this.keyword) > -1
                ){
                  result.push(value)
                }
            })
          }
          this.list=result
        },100)
      }
    },
    mounted () {
      this.scroll =new Bscroll(this.$refs.search)
    }
}
</script>

<style lang="stylus" scoped>
@import '~@/assets/styles/varibles.styl'
  .search
    background $bgColor
    height .72rem
    padding 0 .1rem
    .search-input
      box-sizing border-box
      width 100%
      height .62rem
      line-height .62rem
      padding 0 .1rem
      text-align center
      border-radius .06rem
      color #666
  .search-content
    overflow hidden
    position absolute
    top 1.58rem
    left 0
    right 0
    bottom 0
    background #eeeeee
    z-index 1
    .search-item
      line-height .62rem
      padding-left .2rem
      background #ffffff
      color #666
</style>