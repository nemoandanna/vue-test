<template>
    <div class="todayhot">
        <h3><a href="">今日热点</a></h3>
        <ul>
            <li v-for="(item,i) in todaydata" :key="i">
                <div class="show-list">
                    <div class="imgshow">
                        <a href=""><img :src="item.img" alt=""></a>
                    </div>
                    <div class="hottxt">
                        <h3><a href="">{{item.title}}</a></h3>
                        <p><span>{{item.desc}}</span></p>
                        <p><time>{{item.publishTime}}</time></p>
                    </div>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
    import Vue from 'vue';
    import axios from 'axios';
    export default {
        name:'TodayHot',
        data () {
            return {
                todaydata:[]
            }
        },
        methods:{
            
            getdata () {
                axios.get('/time/Service/callback.mi/PageSubArea/GetFirstPageAdvAndNews.api',{
                    params:{
                        t:20187312113560206
                    }
                }).then((res)=>{
                    console.log(res.data)
                    this.todaydata = res.data.hotPoints;

                })
            },
           
        },
        created() {
            this.getdata();
        },
    }
</script>

<style lang="scss" scoped>

</style>

