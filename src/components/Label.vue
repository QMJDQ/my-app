<template>
        <div class="label">
            <div class="label-top">
                <div class="label-top-top">
                    <div class="title">{{item.biaoti }}</div>
                    <div class="weight">共{{ item.zhongliang }}吨</div>
                </div>
                <div class="label-top-center">
                    <div>{{ item.neirong }}</div>
                </div>
                <div class="label-top-bottom">
                    <div><img src="../assets/01.png" alt=""></div>
                    <div><img src="../assets/02.png" alt=""></div>
                    <div><img src="../assets/03.png" alt=""></div>
                </div>
            </div>
            <div class="label-bottom">
                <div class="label-bottom-top clearfloat" style="margin-bottom: 11px">
                    <img src="../assets/shangjia.png" alt="">
                    <div>供应商：{{ item.gongyingshang }}</div>
                </div>
                <div class="label-bottom-bottom clearfloat">
                    <img src="../assets/shijian.png" alt="">
                    <div>发布时间：{{ item.fabushijian }}</div>
                </div>
            </div>
            <div class="yuan yuan-bottom-left"></div>
            <div class="yuan yuan-bottom-right"></div>
        </div>
</template>

<script>
    export default {
        name: "supply",
        props: {
            item:{
                type: Object,
                default: function () {
                    return {}
                }
            }
        },
        data () {
            return {

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
    .label{
        margin: auto auto 10px auto;
        background-color: white;
        width: 87%;
        border-radius: 5px;
        padding: 20px 15px 13px 15px;
        box-shadow: 0px 6px 20px 0px
        rgba(102, 102, 102, 0.1);
    }
    .label-top-top{
        display: flex;
        justify-content: space-between;
        margin-bottom: 14px;
    }
    .title{
        font-family: PingFang-SC-Bold;
        font-size: 16px;
        font-weight: bold;
        color: #333333;
    }
    .weight{
        font-family: PingFang-SC-Bold;
        font-size: 14px;
        font-weight: bold;
        color: #e4394c;
    }
    .label-top-center{
        font-family: PingFang-SC-Medium;
        font-size: 14px;
        color: #666666;
        line-height: 21px;
    }
    .label-top-bottom{
        display: flex;
        justify-content: space-between;
        margin-top: 11px;
    }
    .label-top-bottom img{
        width: 100px;
        height: 100px;
    }
    .label-top{
        padding-bottom: 16px;
        border-bottom: dashed 1px #d8d8d8;
    }
    .label-bottom{
        padding-top: 15px;
    }
    .label-bottom img{
        width: 15px;
        height: 15px;
        float: left;
        margin-right: 5px;
        margin-top: 1px;
    }
    .label-bottom-top div, .label-bottom-bottom div{
        float: left;
        font-family: PingFang-SC-Regular;
        font-size: 13px;
        color: #666666;
    }
    .yuan{
        width: 14px;
        height: 14px;
        background-color: #f5f4f7;
        border-radius: 100px;
        position: absolute;
    }
    .yuan-top-left{
        top: 363px;
        left: 2px;
    }
    .yuan-top-right{
        top: 363px;
        left: 359px;
    }
    .yuan-bottom-left{
        top: 363px;
        left: 2px;
    }
    .yuan-bottom-right{
        top: 363px;
        left: 359px;
    }
</style>
