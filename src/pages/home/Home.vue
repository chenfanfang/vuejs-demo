<template>
    <div>
        <home-header></home-header>
        <home-swiper></home-swiper>
    </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper';
import axios from 'axios'
export default {
    name: 'Home',
    data() {
        return {
            homeData:{}
        }
    },
    components: {
        HomeHeader,
        HomeSwiper
    },
    methods: {
        getHomeInfo() {
            axios.get('/moc/index.json')
            .then(this.getHomeInfoSuccess)
        },
        getHomeInfoSuccess(res) {
            console.log(res);
            var response = res.data;
            if(response.ret && response.data) {
                this.homeData = response.data;
            }
            
        }
    },
    mounted () {
        this.getHomeInfo();
    }
    
}
</script>

<style lang="stylus" scoped>
    
</style>