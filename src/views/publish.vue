<template>
    <div>
        <div class="header">
            <div class="header-left">
                <img src="../assets/left.png" alt="">
            </div>
            <div class="header-center">{{ title }}</div>
            <div class="header-right">{{ sub }}</div>
        </div>
        <div class="tag">
            <div class="tag-left">{{ tagLeft }}</div>
            <hr/>
            <div class="tag-center">{{ tagCenter }}</div>
            <div class="tag-right">{{ tagRight }}</div>
        </div>
        <PublishTable></PublishTable>
    </div>
</template>

<script>
    import PublishTable from '@/components/PublishTable.vue'
    export default {
        name: "publish",
        data () {
            return {
                title: '发布供需',
                sub: '提交',
                tagLeft: '发布供应',
                tagCenter: '发布需求',
                tagRight: '发布物流',
                category: '类别',
                name: '名称',
                weight: '重量',
                unitprice: '单价',
                address: '选择地址',
                detailedaddress: '详细地址',
                photo: '上传图片',
                introduce: '介绍',
                leibie: '设备（旧）',
                mingcheng: '请输入货物名称',
                zhongliang: '请输入货物重量（KG）',
                danjia: '请输入货物单价（KG）',
                dizhi: '请选择地址',
                xiangxidizhi: '请输入详细地址',
                jieshao: '请简要阐述产品（限200字）'
            }
        },
        methods: {

        },
        created () {

        },
        components: {
            PublishTable
        },
    }
</script>

<style scoped>
    .header{
        display: flex;
        justify-content: space-between;
        padding: 14px 15px;
        align-items: center;
        border-bottom: #f6f5f8 1px solid;
    }
    .header-left img{
        width: 16px;
        height: 16px;
    }
    .header-center{
        font-family: PingFang-SC-Medium;
        font-size: 16px;
        font-weight: normal;
        font-stretch: normal;
        letter-spacing: 0px;
        color: #333333;
    }
    .header-right{
        font-family: PingFang-SC-Bold;
        font-size: 15px;
        font-weight: normal;
        font-stretch: normal;
        letter-spacing: 0px;
        color: #333333;
    }
    .tag{
        display: flex;
        justify-content: space-between;
        padding: 16px 30px;
        font-family: PingFang-SC-Medium;
        font-size: 14px;
        font-weight: normal;
        font-stretch: normal;
        letter-spacing: 0px;
        color: #999999;
        border-bottom: #f6f5f8 10px solid;
    }
    .tag-left{
        font-family: PingFang-SC-Medium;
        font-size: 15px;
        font-weight: normal;
        font-stretch: normal;
        letter-spacing: 0px;
        color: #ff8758;
    }
    .tag hr{
        position: absolute;
        width: 32px;
        height: 3px;
        margin-left: 13px;
        margin-top: 30px;
        background: linear-gradient(-90deg, #fe4e55 0%, #ffb127 100%);
        border: none;
    }
    .tab-label-title{
        font-family: PingFang-SC-Medium;
        font-size: 14px;
        font-weight: normal;
        font-stretch: normal;
        letter-spacing: 0px;
        color: #333333;
        margin-right: 75px;
    }
    .tab-label{
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 18px 0;
        margin: 0 20px;
        border-bottom: #e5e5e5 1px solid;
    }
    .tab img{
        width: 5px;
        height: 10px;
    }
    .tab-category-placeholder{
        font-family: PingFang-SC-Medium;
        font-size: 13px;
        font-weight: normal;
        font-stretch: normal;
        letter-spacing: 0px;
        color: #333333;
    }
    .tab-other-placeholder{
        font-family: PingFang-SC-Medium;
        font-size: 13px;
        font-weight: normal;
        font-stretch: normal;
        letter-spacing: 0px;
        color: #999999;
    }
    .tab-more-title{
        margin-right: 48px;
    }
    .tab-style{
        display: flex;
    }
    .tab-photo, .tab-introduce{
        display: block;
    }
    .tab-photo-title, .tab-introduce-title{
        margin-bottom: 10px;
    }
    .tab-introduce{
        border-bottom: none;
    }
    .tab-photo-img{
        display: flex;
        justify-content: space-between;
    }
    .tab-photo-img img{
        width: 80px;
        height: 80px;
    }
</style>
