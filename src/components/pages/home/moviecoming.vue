<template>
    
</template>
<script>
    import Vue from 'vue';
    import axios from 'axios';
    export default {
        name:'MovieComming',
        data () {
            return {
                topdata:[]
            }
        },
        methods: {
            gettopdata () {
                axios.get('/time/Service/callback.mi/Movie/MovieComingNew.api',{
                    params:{
                        locationId:365,
                   }
                }).then((res)=>{
                    console.log(res.data)
                })
            }
        },
        created () {
            this.gettopdata();
        }
    }

</script>
<style>

</style>
