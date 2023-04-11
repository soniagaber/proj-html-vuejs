<script>
import AppHeader from './components/AppHeader.vue'
import AppDownload from './components/AppDownload.vue'
import MostPopular from './components/MostPopular.vue'
import MenuCategories from './components/MenuCategories.vue'
import LatestNews from './components/LatestNews.vue'
import AppFooter from './components/AppFooter.vue'

export default{
  data(){
    return{};
  },
  components:{
    AppHeader,
    MostPopular,
    AppDownload,
    MenuCategories,
    LatestNews,
    AppFooter
  }
}
</script>

<template>
  <AppHeader></AppHeader>
  <MostPopular></MostPopular>
  <MenuCategories></MenuCategories>
  <AppDownload></AppDownload>
  <LatestNews></LatestNews>
  <AppFooter></AppFooter>
</template>

<style scoped lang="scss">
</style>
