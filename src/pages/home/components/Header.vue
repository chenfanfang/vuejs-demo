<template>
    <div class="header">
        <div class="left">
            <div class="iconfont back-icon">&#xe624;</div>
        </div>
        <div class="middle">
            <span class="iconfont search-icon">&#xe632;</span>
            <input type="text" class="input" placeholder="输入城市/景点/游玩主题">
        </div>
        <router-link to="/city">
            
            <div class="right">
                上海
                <span class="iconfont arrow-icon">&#xe64a;</span>
            </div>
            
        </router-link>
    </div>
</template>

<script>
export default {
    
}
</script>


<style lang="stylus" scoped>
$navHeight = 0.86rem
$navColor = #00bcd4
$verticalMargin = 0.2rem

.header
    background-color $navColor
    line-height $navHeight
    display flex
    .left
        width 0.64rem
        background-color #red
        .back-icon
            font-size 0.3rem
            text-align center
            color white
         
    .right
        min-width 1.4rem
        color white
        text-align center
        .arrow-icon
            font-size .24rem

    
    .middle
        position relative
        flex 1
        display flex
        .search-icon
            position absolute
            left 0.2rem

        .input
            flex 1
            border-radius 0.1rem
            color #ccc
            padding-left 0.7rem
            margin-top 0.1rem
            margin-bottom 0.1rem
            color black
    
</style>