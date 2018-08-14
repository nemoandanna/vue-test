<template>
    <div class="shopmid">
        <a href="">
            <img :src="imgurl" alt="">
        </a>
    </div>
</template>
<script>
import Vue from 'vue'
import axios from 'axios';

    export default {
        name:'MovieAdv',
        data () {
            return {
                advdata:[],
                imgurl:'',
            }
        },
        methods:{
            getadv () {
                axios.get('/time/Service/callback.mi/PageSubArea/MallAreaFirstH5Url.api',{
                    params:{
                        t:'201873120412680323'
                    }
                }).then((res)=>{
                    this.imgurl = res.data.areaFirst.image;
                    // console.log(this.imgurl)
                })
            }
        },
        created() {
            this.getadv()
        },
    }
</script>

<style lang="scss" scoped>
    .shopmid{
        padding-top: 0.2rem;
        padding-bottom: 0.2rem;
        img{
            display: block;
            height: 1.9rem;
            width: 3.75rem;
        }
    }
</style>
