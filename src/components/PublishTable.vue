<template>
    <div class="tab">
        <div class="tab-category tab-label">
            <div class="tab-style">
                <div class="tab-label-title">{{ category }}</div>
                <div class="tab-category-placeholder tab-input">
                    <select v-model="leibie">
                        <option disabled value="设备（旧）">请选择</option>
                        <option>设备（旧）</option>
                        <option>设备（新）</option>
                        <option>设备（不新不旧）</option>
                    </select>
                </div>
            </div>
            <div><img src="../assets/jinrujiantou.png" alt=""></div>
        </div>
        <div class="tab-name tab-label">
            <div class="tab-style">
                <div class="tab-label-title">{{ name }}</div>
                <div class="tab-other-placeholder tab-input"><input v-model="mingcheng" placeholder="请输入货物名称"></div>
            </div>
        </div>
        <div class="tab-weight tab-label">
            <div class="tab-style">
                <div class="tab-label-title">{{ weight }}</div>
                <div class="tab-other-placeholder tab-input"><input v-model="zhongliang" placeholder="请输入货物重量（KG）"></div>
            </div>
        </div>
        <div class="tab-unitprice tab-label">
            <div class="tab-style">
                <div class="tab-label-title">{{ unitprice }}</div>
                <div class="tab-other-placeholder tab-input"><input v-model="danjia" placeholder="请输入货物单价（KG）"></div>
            </div>
        </div>
        <div class="tab-address tab-label">
            <div class="tab-style">
                <div class="tab-label-title tab-more-title">{{ address }}</div>
                <div class="tab-other-placeholder tab-input">{{ dizhi }}</div>
            </div>
            <div><img src="../assets/jinrujiantou.png" alt=""></div>
        </div>
        <div class="tab-detailedaddress tab-label">
            <div class="tab-style">
                <div class="tab-label-title tab-more-title">{{ detailedaddress }}</div>
                <div class="tab-other-placeholder tab-input"><input v-model="xiangxidizhi" placeholder="请输入详细地址"></div>
            </div>
        </div>
        <div class="tab-photo tab-label">
            <div class="tab-photo-title tab-label-title">{{ photo }}</div>
            <div class="tab-photo-img">
                <img src="../assets/01.png" alt="">
                <img src="../assets/02.png" alt="">
                <img src="../assets/03.png" alt="">
                <img src="../assets/04.png" alt="">
            </div>
        </div>
        <div class="tab-introduce tab-label">
            <div class="tab-introduce-title tab-label-title">{{ introduce }}</div>
            <div class="tab-other-placeholder tab-input"><textarea v-model="jieshao" placeholder="请简要阐述产品（限200字）"></textarea></div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "publish",
        data () {
            return {
                category: '类别',
                name: '名称',
                weight: '重量',
                unitprice: '单价',
                address: '选择地址',
                detailedaddress: '详细地址',
                photo: '上传图片',
                introduce: '介绍',
                leibie: '设备（旧）',
                mingcheng: '',
                zhongliang: '',
                danjia: '',
                dizhi: '请选择地址',
                xiangxidizhi: '',
                jieshao: ''
            }
        },
        methods: {

        },
        created () {

        },
        components: {

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
        color: #777777;
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
    input, textarea{
        border: none;
        outline:medium;
    }
    textarea{
        width: 100%;
        height: 70px;
    }
    select{
        border: none;
        outline:medium;
        /*appearance:none;*/
        -moz-appearance:none;
        -webkit-appearance:none;
        width: 200px;
    }
</style>
