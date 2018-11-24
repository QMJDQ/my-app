<template>
    <div class="zong" style="background-color: #f6f5f8">
        <div class="toubu clearfloat">
            <img class="touxiang" src="../assets/touxiang.jpg" alt="">
            <div class="ziliao">
                <div class="name">{{ name }}</div>
                <div class="yinxiang">个人印象：{{ yinxiang }}</div>
            </div>
        </div>
        <div class="xinxi clearfloat">
            <div>
                <div class="phone clearfloat">
                    <img style="float: left" src="../assets/dianhua.png" alt="">
                    <div style="float: left">{{ phone }}</div>
                </div>
                <div class="email">
                    <img style="float: left" src="../assets/youxiang.png" alt="">
                    <div style="float: left">{{ email }}</div>
                </div>
            </div>
            <div class="dizhi">
                <img style="float: left" src="../assets/didian.png" alt="">
                <div style="float: left">{{ dizhi }}</div>
            </div>
        </div>
        <div class="caidanlan">
            <div class="caidan">
                <img class="caidantubiao" src="../assets/pengyouquan.png" alt="">
                <div class="xian">
                    <div class="caidandiv">我的小火车</div>
                    <img class="jinru" src="../assets/jinrujiantou.png" alt="">
                </div>
            </div>
            <div class="caidan">
                <img class="caidantubiao" src="../assets/bangong.png" alt="">
                <div class="xian">
                    <div class="caidandiv">成为服务商</div>
                    <img class="jinru" src="../assets/jinrujiantou.png" alt="">
                </div>
            </div>
            <router-link to="/s" class="caidan">
                <img class="caidantubiao" src="../assets/bianji.png" alt="">
                <div class="xian">
                    <div class="caidandiv">我的发布</div>
                    <img class="jinru" src="../assets/jinrujiantou.png" alt="">
                </div>
            </router-link>
            <div class="caidan">
                <img class="caidantubiao" src="../assets/wuliu.png" alt="">
                <div class="xian">
                <div class="caidandiv">我的物流</div>
                <img class="jinru" src="../assets/jinrujiantou.png" alt="">
                </div>
            </div>
            <div class="caidan">
                <img class="caidantubiao" src="../assets/shoucang.png" alt="">
                <div class="xian">
                    <div class="caidandiv">我的收藏</div>
                    <img class="jinru" src="../assets/jinrujiantou.png" alt="">
                </div>
            </div>
            <div class="caidan" @click="aa">
                <img class="caidantubiao" src="../assets/mima.png" alt="">
                <div class="xian" style="border-bottom: 0 #dddddd solid;">
                    <div class="caidandiv">修改密码</div>
                    <img class="jinru" src="../assets/jinrujiantou.png" alt="">
                </div>
            </div>
        </div>
        <div class="kong"></div>
        <div class="dibu clearfloat">
            <div class="dibuyeqian clearfloat">
                <img class="qita" src="../assets/home.png" alt="">
                <div>首页</div>
            </div>
            <div class="dibuyeqian clearfloat">
                <img class="qita" src="../assets/huoche.png" alt="">
                <div>小火车</div>
            </div>
            <router-link to="/publish" class="dibuyeqian clearfloat">
                <img class="fabu" src="../assets/fabu.png" alt="">
                <div class="fabudiv">发布</div>
            </router-link>
            <div class="dibuyeqian clearfloat">
                <img class="qita" src="../assets/shangmen.png" alt="">
                <div>上门服务</div>
            </div>
            <div class="dibuyeqian clearfloat">
                <img class="qita" src="../assets/gerenS.png" alt="">
                <div>个人中心</div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'HelloWorld',
    props: {
      msg: {
          type: Array,
          default () {
              return []
          }
      }
    },
  data () {
      return {
          name: '王二狗',
          yinxiang: '旅游达人，豁达',
          phone: '18653292740',
          email: '675730681@qq.com',
          dizhi: '青岛市崂山区株洲路153号'
      }
  },
    methods: {
        aa () {
            this.$emit('msg',111);
        }
    },
    created () {

    }
}
</script>

<style scoped>
    .clearfloat:after{display:block;clear:both;content:"";visibility:hidden;height:0}
    .clearfloat{zoom:1}
    *{
        /*background-color: #ffffff;*/
    }
    .toubu{
        height: 106px;
        background: linear-gradient(to right,#ffcd4e, #ffa964);
    }
    .touxiang{
        float: left;
        width: 58px;
        height: 58px;
        margin-left: 17px;
        margin-top: 15px;
        border-radius: 100px;
    }
    .ziliao{
        float: left;
        margin-left: 10px;
        margin-top: 26px;
    }
    .name{
        font-size: 14px;
        color: white;
    }
    .yinxiang{
        font-size: 12px;
        margin-top: 10px;
        color: white;
    }
    .xinxi{
        width: 80%;
        color: #666666;
        padding: 5%;
        margin: -17px auto 10px;
        background-color: #ffffff;
        box-shadow: 0px 6px 20px 0px
        rgba(102, 102, 102, 0.21);
        border-radius: 10px;
    }
    .phone img, .email img, .dizhi img{
        width: 14px;
        height: 14px;
        margin-right: 8px;
    }
    .phone, .email,.dizhi{
        font-size: 12px;
    }
    .phone, .dizhi{
        float: left;
    }
    .email{
        float: right;
    }
    .phone, .email{
        margin-bottom: 14px;
    }
    .caidanlan{
        margin: auto;
        width: 80%;
        padding: 7px 17px 7px 17px;
        background-color: white;
        border-radius: 10px;
        font-family: PingFang-SC-Medium;
        font-size: 14px;
        color: #333333;
    }
    .caidan{
        height: 40px;
        display: flex;
        align-items: center;
        text-decoration: none;
        color: #333333;
    }
    .caidantubiao{
        width: 15px;
        height: 15px;
        margin-right: 17px;
    }
    .xian{
        height: 40px;
        display:flex;
        flex-grow: 1;
        align-items: center;
        justify-content: space-between;
        border-bottom: 0.5px #dddddd solid;
    }
    .jinru{
        width: 5px;
        height: 9px;
        margin-top: 5px;
    }
    .kong{
        padding: 23%;
    }
    .dibu{
        width: 100%;
        background-color: #ffffff;
        height: 50px;
        /*padding-top: 10px;*/
        font-size: 10px;
        color: #999999;
        padding: auto 15px auto 27px;
        text-align: center;
        position: fixed;
        bottom: 0px;
        display: flex;
        justify-content: space-between;
    }
    .dibuyeqian{
        /*position: relative;*/
        /*float: left;*/
        margin-left: 4%;
        margin-right: 4%;
        text-align: center;
        text-decoration:none;
        color: #999999;
    }
    .qita{
        width: 22px;
        height: 22px;
    }
    .fabu{
        position: relative;
        top: -40px;
        width: 55px;
        height: 55px;
        background-color: #ffffff;
        border-radius: 100px;
    }
    .fabudiv{
        margin-top: -33px;
    }
</style>
