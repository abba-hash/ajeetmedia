<template lang="">
    <SearchVue/>
    <CategoryVue/>
    <ArticlesVue/>
</template>
<script>
import SearchVue from '@/components/Search.vue'
import CategoryVue from '@/components/Category.vue'
import ArticlesVue from '@/components/Articles.vue'
export default {
    name:'BlogView',
    components:{
        SearchVue,
        CategoryVue,
        ArticlesVue
    }
}
</script>
<style lang="scss">
    
</style>