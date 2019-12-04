<template>
    <div>
      <city-header></city-header>
      <city-search></city-search>
      <city-list></city-list>
    </div>
</template>

<script>
import CityHeader from './componets/Header'
import CitySearch from './componets/Search'
import CityList from './componets/List'
export default {
    name:'City',
    components:{
        CityHeader,
        CitySearch,
        CityList
    }
}
</script>

<style lang="stylus" scoped>

</style>