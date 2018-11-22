<template>
    <div>
        <div class="search">
            <div class="search-inner">
                <img class="search-icon" src="../assets/search_icon.png" alt="">
                <span>{{ sousuo }}</span>
            </div>
        </div>
        <div class="sort">
            <div>
                <span style="color: #ff8758;">时间排序</span>
                <img class="sort-icon" src="../assets/shang.png" alt="">
                <img class="sort-icon" style="margin-left: -12px" src="../assets/xiaR.png" alt="">
                <hr/>
            </div>
            <div>
                <span style="color: #999999;">距离排序</span>
                <img class="sort-icon" src="../assets/shang.png" alt="">
                <img class="sort-icon" style="margin-left: -12px" src="../assets/xia.png" alt="">
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "supply",
        props: {

        },
        data () {
            return {
                sousuo: '搜索'
            }
        },
        methods: {

        },
        created () {

        }
    }
</script>

<style scoped>
    .clearfloat:after{display:block;clear:both;content:"";visibility:hidden;height:0}
    .clearfloat{zoom:1}
    *{
        margin: 0;
        padding: 0;
    }
    .search{
        background-color: #ffffff;
        padding: 7px 20px;
        margin-bottom: 1px;

    }
    .search-inner{
        /*width: 710px;*/
        height: 28px;
        background-color: #eeeeee;
        border-radius: 14px;
        display: flex;
        align-items: center;
    }
    .search-icon{
        width: 15px;
        height: 15px;
        margin-left: 15px;
        margin-right: 10px;
    }
    .search-inner span{
        font-size: 12px;
        color: #999999;
        opacity: 0.9;
    }
    .sort{
        background-color: white;
        display: flex;
        justify-content: space-between;
        padding: 10px 65px 0 65px;
        font-family: PingFang-SC-Medium;
        font-size: 15px;
        margin-bottom: 10px;
    }
    .sort-icon{
        width: 12px;
        height: 12px;
    }
    .sort hr{
        width: 32px;
        height: 3px;
        margin-left: 14px;
        margin-top: 10px;
        background: linear-gradient(-90deg, #fe4e55 0%, #ffb127 100%);
        border: none;
    }
</style>
