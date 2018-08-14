
<template>
    <div id="app-home">
        <app-index-top></app-index-top>
        <movie-now></movie-now>
        <movie-adv></movie-adv>
        <today-hot></today-hot>
    </div>
</template>

<script>
    import AppIndexTop from './index-top';
    import MovieNow from './movienow';
    import MovieAdv from './movie-adv';
    import TodayHot from './todayhot';
    export default {
        name:'AppHome',
        components:{
            'app-index-top':AppIndexTop,
            'movie-now':MovieNow,
            'movie-adv':MovieAdv,
            'today-hot':TodayHot,
        }
    }
</script>

<style>

</style>
