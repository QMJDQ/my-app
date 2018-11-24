<template>
    <div>
        <div class="header">
            <router-link to="/" class="header-left">
                <img src="../assets/left.png" alt="">
            </router-link>
            <div class="header-center">{{ title }}</div>
            <div class="header-right">{{ sub }}</div>
        </div>
        <div class="tag">
            <div class="tag-left">{{ tagLeft }}</div>
            <div class="tag-center">{{ tagCenter }}</div>
            <div class="tag-right">{{ tagRight }}</div>
            <hr/>
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
    *{
        margin: 0;
        padding: 0;
    }
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
</style>
