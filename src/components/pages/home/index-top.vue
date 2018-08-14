<template>
    <div class="head-nav">
        <ul class="table-list">
            <li class="table-item"><i><img src="http://static1.mtime.cn/html5/20180727153608/images/2014/logo_mtime.png" alt=""></i></li>
            <li class="table-item"><a href=""><span>首页</span></a></li>
            <li class="table-item"><a href=""><span>购票</span></a></li>
            <li class="table-item"><a href=""><span>商城</span></a></li>
            <li class="table-item"><a href=""><span>发现</span></a></li>
            <li class="table-item"><a href=""><img src="http://static1.mtime.cn/html5/20180727153608/images/2014/ico_my.png" alt=""></a></li>
        </ul>
    </div>
</template>

<script>
    export default{
        name:'app-index-top'
    }
</script>

<style lang="scss" scoped>
    .head-nav{
        background: #1c2635;
        ul{
            display: flex;
            li{
                padding: 0.1rem 0.135rem;
                
                i{
                    img{
                        display: inline-block;
                        width: 0.67rem;
                        height: 0.22rem;
                    }
                }
                a{
                    font-size: 0.16rem;
                    color:white;
                    img{
                        display: inline-block;
                        width: 0.168rem;
                        height: 0.2159rem;
                    }
                }
            }
        }
    }
</style>

