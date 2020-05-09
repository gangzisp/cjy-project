<template>
    <div class="home">
        <home-swiper :banners="banners" />
        <list-item :listDatas="listDatas" />
    </div>
</template>
<script>
    import { getHomeMultidata } from "../../service/home"

    import HomeSwiper from './childComps/HomeSwiper'
    import ListItem from '../../components/ListItem'
    
    export default {
        name: 'Home',
        components: {
            HomeSwiper,
            ListItem
        },
        data() {
            return {
                banners: null,
                listDatas: null,
            }
        },
        
        created() {
            getHomeMultidata().then(res=> {
                console.log(res)
                this.banners = res.data.slide;
                this.listDatas = res.data.list;
            }).catch(err=> {
                console.log(err)
            }) 
        }
    }
</script>
<style>
    
</style>