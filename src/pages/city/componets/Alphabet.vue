<template>
    <ul class="list">
        <li class="item"
            v-for="item of letters"
            :key="item"
            :ref="item"
            @click="handleletterClick"
            @touchstart="handleTouchStart"
            @touchmove="handleTouchMove"
            @touchend="handleTouchEnd"
            >{{item}}</li>
    </ul> 
</template>

<script>
export default {
    name:'CityAlphabet',
    props:{
        cities:Object
    },
    computed:{
        letters (){
            const letters = []
            for(let i in this.cities) {
                letters.push(i)
            }
            return letters
        }
    },
    data () {
        return{
            touchStatus: false
        }
    },
    methods:{
        handleletterClick (e){
            this.$emit('change',e.target.innerText)
        },
        handleTouchStart (){
            this.touchStatus = true
        },
        handleTouchMove (e){
            const startY = this.$refs['A'][0].offsetTop
            const touchY = e.touches[0].clientY - 80
            const index = Math.floor((touchY - startY)/20)
            if (index >=0 && index < this.letters.length){
                this.$emit('change',this.letters[index])
            }
            console.log(index)
        },
       handleTouchEnd (){
           this.touchStatus = false
       } 
    }
}
</script>

<style lang="stylus" scoped>
@import '~@/assets/styles/varibles.styl'
    .list
      display flex
      flex-direction column
      justify-content center
      position absolute
      top 1.58rem
      right 0
      bottom 0
      width .4rem
      .item
        text-align center
        line-height .4rem
        color $bgColor
</style>