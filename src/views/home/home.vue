<template>
    <div class="home">
        主页
    </div>
</template>
<script>
    import { getHomeMultidata } from "../service/home"
    // import HomeSwiper from './childComps/HomeSwiper'
    
    export default {
        name: 'Home',
        components: {
            // HomeSwiper,
        },
        data() {
            return {
                banners: null,
                listDatas: null,
            }
        },
        
        created() {
            getHomeMultidata().then(res=> {
                console.log('res',res)
            }).catch(err=> {
                console.log(err)
            }) 
        }
    }
</script>
<style>
    
</style>