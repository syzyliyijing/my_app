<template>
     <div>
         <home-header></home-header>
         <home-swiper></home-swiper>
         <home-icons></home-icons>
         <home-hot></home-hot>
         <home-liked></home-liked>
         <home-weekend></home-weekend>
     </div>
</template>

<script>
import HomeHeader from './componets/header'
import HomeSwiper from './componets/Swiper'
import HomeIcons from './componets/Icons'
import HomeHot from './componets/Hot'
import HomeLiked from './componets/Liked'
import HomeWeekend from './componets/Weekend'
export default {
  name: 'Home',
  components:{
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeHot,
    HomeLiked,
    HomeWeekend
  }
}
</script>

<style scoped>

</style>