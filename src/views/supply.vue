<template>
    <div class="zong">
        <div class="header">
            <router-link to="/" class="header-left"><img src="../assets/zuo.png" alt=""></router-link>
            <div class="header-right-style">
                <div class="header-right">
                    <div :class="headerRight?'header-right-left-l':'header-right-right-r'" class="header-right-left" @click="lshow">供应列表</div>
                    <div :class="headerRight?'header-right-right-r':'header-right-right-l'" class="header-right-right" @click="lnshow">需求列表</div>
                </div>
            </div>
        </div>
        <Search/>
        <div v-if="show==='label'">
            <Label v-for="(aa,index) in list" :item = 'aa' :key="index"></Label>
        </div>
        <div v-else>
            <Label v-for="(bb,index) in needlist" :item = 'bb' :key="index"></Label>
        </div>
        <div class="kong"></div>
    </div>
</template>

<script>
    import Label from '@/components/Label.vue'
    import Search from '@/components/Search.vue'
    export default {
        name: "supply",
        data () {
            return {
                show: 'label',
                headerRight: true,
                list: [
                    {
                        biaoti: '运送20吨废旧钢铁',
                        zhongliang: '200',
                        neirong: '废旧钢铁出售，共200吨，质量上乘，价格公道！童叟无欺！要的赶快联系我',
                        gongyingshang: '青岛钢材有限公司',
                        fabushijian: '2018-09-27',
                    },
                    {
                        biaoti: '运送20吨废旧钢铁',
                        zhongliang: '200',
                        neirong: '废旧钢铁出售，共200吨，质量上乘，价格公道！童叟无欺！要的赶快联系我',
                        gongyingshang: '青岛钢材有限公司',
                        fabushijian: '2018-09-27',
                    },
                    {
                        biaoti: '运送20吨废旧钢铁',
                        zhongliang: '200',
                        neirong: '废旧钢铁出售，共200吨，质量上乘，价格公道！童叟无欺！要的赶快联系我',
                        gongyingshang: '青岛钢材有限公司',
                        fabushijian: '2018-09-27',
                    },
                    {
                        biaoti: '运送20吨废旧钢铁',
                        zhongliang: '200',
                        neirong: '废旧钢铁出售，共200吨，质量上乘，价格公道！童叟无欺！要的赶快联系我',
                        gongyingshang: '青岛钢材有限公司',
                        fabushijian: '2018-09-27',
                    }
                ],
                needlist: [
                    {
                        biaoti: '我想运送20吨废旧钢铁',
                        zhongliang: '200',
                        neirong: '废旧钢铁回收，共200吨，质量上乘，价格公道！童叟无欺！有的赶快联系我',
                        gongyingshang: '青岛钢材有限公司',
                        fabushijian: '2018-09-27',
                    },
                    {
                        biaoti: '我想运送20吨废旧钢铁',
                        zhongliang: '200',
                        neirong: '废旧钢铁回收，共200吨，质量上乘，价格公道！童叟无欺！有的赶快联系我',
                        gongyingshang: '青岛钢材有限公司',
                        fabushijian: '2018-09-27',
                    },
                    {
                        biaoti: '我想运送20吨废旧钢铁',
                        zhongliang: '200',
                        neirong: '废旧钢铁回收，共200吨，质量上乘，价格公道！童叟无欺！有的赶快联系我',
                        gongyingshang: '青岛钢材有限公司',
                        fabushijian: '2018-09-27',
                    },
                    {
                        biaoti: '我想运送20吨废旧钢铁',
                        zhongliang: '200',
                        neirong: '废旧钢铁回收，共200吨，质量上乘，价格公道！童叟无欺！有的赶快联系我',
                        gongyingshang: '青岛钢材有限公司',
                        fabushijian: '2018-09-27',
                    }
                ]
            }
        },
        methods: {
            lnshow: function () {
                if (this.show==='label') {
                    this.show = 'labelneed';
                    this.headerRight = false
                }
            },
            lshow: function () {
                if (this.show==='labelneed') {
                    this.show = 'label';
                    this.headerRight = true
                }
            }
        },
        created () {

        },
        components: {
            Label,
            Search
        },
    }
</script>

<style scoped>
    .clearfloat:after{display:block;clear:both;content:"";visibility:hidden;height:0}
    .clearfloat{zoom:1}
    *{
        margin: 0;
        padding: 0;
    }
    .zong{
        background-color: #f5f4f7;
    }
    .header{
        display: flex;
        align-items: center;
        text-align: center;
        font-family: PingFang-SC-Medium;
        font-size: 13px;
        height: 44px;
        padding-left: 15px;
        background-color: white;
        margin-bottom: 0.5px;
    }
    .header-right-style{
        margin-left: -31px;
        display: flex;
        flex-grow: 1;
        justify-content: center;
    }
    .header-left{
        margin-top: 5px;
    }
    .header-left img{
        width: 16px;
        height: 16px;
    }
    .header-left, .header-right{
        float: left;
    }
    .header-right{
        height: 30px;
        border-radius: 5px;
        border: solid 0.5px #ff8758;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .header-right-left, .header-right-right{
        padding: 7px 15px;
    }
    .header-right-left-l{
        background-color: #ff8758;
        border-radius: 5px 0 0 5px;
        color: #ffffff;
    }
    .header-right-left-r{
        color: #ff8758;
        border-radius: 0 5px 5px 0;
    }
    .header-right-right-l{
        background-color: #ff8758;
        border-radius: 0 5px 5px 0;
        color: #ffffff;
    }
    .header-right-right-r{
        border-radius: 5px 0 0 5px;
        color: #ff8758;
    }
    .kong{
        padding: 3%;
    }
</style>
