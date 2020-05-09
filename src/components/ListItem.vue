<template>
    <div>
        <a class="list-box"  v-for="(item,index) in listDatas" :key="index" :href="item.url">
            <div class="list-img">
                <img :src="item.cover" alt="">
            </div>
            <div class="list-text-box">
                <h4>{{ item.title }}</h4>
                <p>{{ item.published }}</p>
            </div>
        </a>
    </div>
    
</template>
<script>
    export default {
        name: 'ListItem',
        props: {
            listDatas: {
                type: Array,
                default() {
                    return []
                }
            }
        },
        mounted() {
            console.log(this.listDatas)
        }
    }
</script>
<style scoped>
    .list-box {
        display: flex;
        padding: 10px;
    }
    .list-img {
        width: 20%;
    }
    .list-img img{
        width: 100%;
    }
    .list-text-box {
        display: flex;
        padding-left: 10px;
        font-size: 14px;
        color: #333;
        flex: 1;
        flex-direction: column;
        justify-content: space-between;
    }
    .list-text-box p {
        font-size: 12px;
        color: #999;
    }
</style>