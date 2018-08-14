<template>  
    <div class="movienow-list">
        <h2><a href=""><b>正在热映({{topdata.length}})</b></a></h2>
        <ul>
            <li v-for="(item,i) in topdata" :key="i" v-if="i<=7">
                <div class="mpic"><a href=""><img :src="item.img" alt=""></a></div>
                <i v-if="i<=3">{{item.r}}</i>
                <p><span>{{item.t}}</span></p>
            </li>
        </ul>
        <h3><a href=""><b>即将上映()</b></a></h3>
    </div>
</template>
<script>
    import Vue from 'vue';
    import axios from 'axios';
    export default {
        name:'MovieNow',
        data () {
            return {
                topdata:[]
            }
        },
        methods: {
            gettopdata () {
                axios.get('/time/Service/callback.mi/Showtime/LocationMovies.api',{
                    params:{
                        locationId:365,
                   }
                }).then((res)=>{
                    this.topdata = res.data.ms;
                    // console.log(this.topdata)
                })
            }
        },
        created () {
            this.gettopdata();
        }
    }

</script>
<style lang="scss" scoped>
    .movienow-list{
        background: white;
        h2{
            text-align: left;
            padding: 0.1rem;
            b{
                font-size: 0.2rem;
                color:#333;
                font-weight: bold;
            }
        }
        h3{
            margin-top: 0.15rem;
            text-align: left;
            padding: 0.2rem 0;
            margin-left: 0.1rem;
            border-top: 1px solid #d8d8d8;
       
            b{
                font-size: 0.2rem;
                color:#333;
                font-weight: bold; 
            }
        }
        ul{
            padding: 0.06rem 0.1rem;
            display: flex;
            flex-wrap: wrap;
            li{
                position: relative;
                width: 25%;
                &:nth-child(n+5){
                    margin-top: 0.15rem;
                }
                .mpic{
                    width: 0.78rem;
                    img{
                        display: inline-block;
                        height: 1.16rem;
                        width: 100%;
                        
                }
                }
                i{
                    display: block;
                    background: #659d0e;
                    width: 0.24rem;
                    height: 0.24rem;
                    padding: 0.04rem;
                    color:white;
                    position: absolute;
                    top: 0.04rem;
                    right: 0.15rem;
                }
                p{
                    padding-right: 0.1rem;
                    span{
                        display: inline-block;
                        width: 0.78rem;
                        overflow: hidden;
                        text-overflow:ellipsis;
                        white-space: nowrap;
                    }
                }
            }
        }
    }
</style>

