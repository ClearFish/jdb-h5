<script setup>
import { ref } from 'vue'
import game1 from "@/assets/home/game1.png"
let webs = ref([
  {label:'站点一',name:'djdkfjfnk.com',value:'https://djdkfjfnk.com'},
  {label:'站点二',name:'djdkfjfnk.com',value:'https://djdkfjfnk.com'},
  {label:'站点三',name:'djdkfjfnk.com',value:'https://djdkfjfnk.com'}
])
let games = ref([
  {name:'1',url:'',img:game1},
  {name:'1',url:'',img:game1},
  {name:'1',url:'',img:game1},
  {name:'1',url:'',img:game1},
  {name:'1',url:'',img:game1},
  {name:'1',url:'',img:game1}
])
let vipLists = ref([
  {name:'天天红包雨',url:''},
  {name:'签到领现金',url:''},
  {name:'借呗免息',url:''},
  {name:'周礼金',url:''},
  {name:'月礼金',url:''},
  {name:'亏损救援',url:''}
])

const count = ref(0)
</script>

<template>
<div class="big_box">
  <div class="top_box">
    <img src="@/assets/home/logo.png" alt="" class="logo">
    <img src="@/assets/home/human_bg.png" alt="" class="human">
    <div class="word">
      <div class="top">
        <img src="@/assets/home/JDB.png" alt="" class="title1">
        <img src="@/assets/home/slots.png" alt="" class="title2">
      </div>
      <img src="@/assets/home/title.png" alt="" class="title3">
    </div>
    <div class="box2">
      <div class="cont">
        <div class="left">
          <img src="@/assets/home/logo_left.png" alt="">
        </div>
        <div class="right">
          <div class="top">
            <p class="word_t">JDB棋牌</p>
            <p class="name">官网</p>
          </div>
          <div class="middle">
            <img src="@/assets/home/star.svg" alt="" v-for="(item,index) in (new Array(5).fill(0))">
            <p>9783万+</p>
          </div>
          <div class="download">
            <div class="left_d">
              <img src="@/assets/home/download.svg" alt="">
              <p class="num">100.18万</p>
            </div>
             <div class="left_d">
              <img src="@/assets/home/phone.svg" alt="">
              <p class="num">IOS&Android</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="download_box">
    <img src="@/assets/home/ios_download.png" alt="">
     <img src="@/assets/home/andrid_download.png" alt="">
  </div>
  <img src="@/assets/home/bg_3.png" alt="" class="poster">
    <div class="types_container ">
    <div class="title">
      <img src="@/assets/home/bg_4.png" alt="">
    </div>
    <div class="list_box">
      <div class="list_item" v-for="(item,index) in webs" :key="index">
        <div class="left">
          <p class="label">{{item.label}}</p>
          <p class="value">{{item.name}}</p>
        </div>
        <div class="btn">点击进入</div>
      </div>
    </div>
  </div>
  <div class="types_container add_margin">
    <div class="title">
      <img src="@/assets/home/bg_5.png" alt="">
    </div>
    <div class="game_box">
      <div class="game_item" v-for="(item,index) in games" :key="index">
       <img :src="item.img" alt="">
      </div>
    </div>
  </div>
    <div class="types_container add_margin">
    <div class="title">
      <img src="@/assets/home/bg_6.png" alt="">
    </div>
    <div class="content_vip">
      <div class="left">
        <div class="top_ttile">
          <img src="@/assets/home/vip_title.png" alt="">
          <p class="sub">注册领工资最高领<span>8666</span>元</p>
        </div>
        <div class="middle_lists">
          <div class="middle_item" v-for="(item,index) in vipLists" :key="index">
            <p>
              {{item.name}}
            </p>
          </div>
        </div>
        <div class="bottom">
          <img src="@/assets/home/bottom_bg.png" alt="">
        </div>
      </div>
      <div class="right">
        <img src="@/assets/home/vip.png" alt="">
      </div>
    </div>
  </div>
  <div class="bottom_foot">
    <div class="left">
      <img src="@/assets/home/logo_left.png" alt="">
    </div>
    <div class="center">
      <p class="first">下载手机APP</p>
      <p class="sec">注册即送<span>80~588</span>元</p>
      <div class="third">
        <img src="@/assets/home/star.svg" alt="" v-for="(item,index) in (new Array(5).fill(0))">
        <p>1.3亿+ 玩家首选</p>
      </div>
      
    </div>
    <div class="right">
        <img src="@/assets/home/download_now.png" alt="">
      </div>
  </div>
  <div class="servoce_box">
    <img src="@/assets/home/service.png" alt="">
  </div>
</div>

  
</template>

<style scoped lang="scss">
.big_box {
    width: 100%;
    min-height: 100vh;
    background: #010101;
    padding-bottom: 80px;
    position: relative;
    .top_box {
      width: 100%;
      height: 518px;
      background: url('@/assets/home/top_bg.png') no-repeat center;
      background-size: 100% 100%;
      padding-top: 68px;
      position: relative;
      .logo {
        width: 133px;
      }
      .human {
        margin-top: -50px;
      }
      .word {
        width: 100%;
        position: absolute;
        bottom: 200px;
        left: 0;
        .top {
          width: 100%;
           display: flex;
           justify-content: center;
            .title1 {
              width: 99px;
              height: 48px;
            }
            .title2 {
              width: 100px;
              height: 50px;
            }
        }
        .title3 {
          width: calc(100% - 40px);
          height: auto;
          margin-top: -10px;
        }
      }
      .box2 {
        width: 100%;
        height: 186px;
        // background: url('@/assets/home/shadow.png')  no-repeat center;
        // background-size: 100% 100%;
        background-image: linear-gradient(180deg,rgba(194,1,105,0),#000 14%);
        box-shadow: 0 0.048rem 0.16rem 0 rgba(6,10,14,.15);
        position: absolute;
        bottom: 0;
        z-index: 0;
        display: flex;
        justify-content: center;
        align-items: center;
        .cont {
          width: calc(100% - 40px);
          height: 134px;
          background: url('@/assets/home/bg_2.png') no-repeat center;
          background-size: 100% 100%;
          display: flex;
          align-items: center;
          justify-content: center;
          gap: 17px;
          .left {
            img {
              width: 92px;
              height: 92px;
            }
          }
          .right {
            .top {
              display: flex;
              gap: 14px;
              align-items: center;
              .word_t {
                  color: #FAFCCC;
                  font-family: Alibaba PuHuiTi;
                  font-size: 24px;
                  font-style: normal;
                  font-weight: 500;
              }
              .name {
                height: 20px;
                width: 38px;
                border-radius: 22px;
                background: linear-gradient(180deg, #F00 16.67%, #B50000 100%);
                text-align: center;
                line-height: 20px;
                color: #FFF;
                font-family: PingFang SC;
                font-size: 12px;
                font-style: normal;
                font-weight: 600;
              }
            }
            .middle {
              display: flex; 
              align-items: center;
              margin-top: 4px;
              gap: 6px;
              color: #FFF;
              font-family: PingFang SC;
              font-size: 14px;
              font-style: normal;
              font-weight: 500;
            }
            .download {
              display: flex;
              align-items: center;
              margin-top: 4px;
              gap: 12px;
              .left_d {
                display: flex;
                align-items: center;
                gap: 2px;
                color: #FFF;
                opacity: 0.6;
                font-family: PingFang SC;
                font-size: 12px;
                font-style: normal;
                font-weight: 400;
              }
            }
          }
        }
      }
    }
    .download_box {
      display: flex;
      align-items: center;
      justify-content: center;
      gap:20px;
      width: calc(100% - 40px);
      margin: 0 auto;
      img {
       width: 50%;
      }
    }
    .poster {
      width: calc(100% - 40px);
      margin: 0 auto;
      margin-top: 20px;
      border-radius: 10px;
      border: 4px solid #F8DF85;
    }
    .types_container {
      width: 100%;
      margin-top: 20px;
      .title {
        width: 100%;
        img {
          width: calc(100% - 60px);
          margin: 0 auto;
        }
      }
      .list_box {
        width: calc(100% - 40px);
        margin: 0 auto;
        margin-top: 10px;
        .list_item {
          width: 100%;
          display: flex;
          align-items: center;
          justify-content: space-between;
          gap: 10px;
          margin-bottom: 13px;
          .left {
            flex: 1;
            display: flex;
            height: 30px;
            align-items: center;
            border: 1px solid #AEA288;
            .label {
              height: 100%;
              width: 75px;
              text-align: center;
              border-right: 1px solid #AEA288;
              line-height: 30px;
              color: #FFF;
              opacity: 0.8;
              font-family: PingFang TC;
              font-size: 13px;
              font-style: normal;
              font-weight: 500;
            }
            .value {
              padding-left: 17px;
              box-sizing: border-box;
              color: #FFF;
              opacity: 0.8;
              font-family: PingFang TC;
              font-size: 13px;
              font-style: normal;
              font-weight: 500;
            }
          }
          .btn {
            width: 70px;
            height: 30px;
            border-radius: 4px;
            background: linear-gradient(99deg, #F8DF85 9.2%, #F1B753 97.17%);
            display: flex;
            justify-content: center;
            align-items: center;
            color: #000;
            font-family: PingFang TC;
            font-size: 13px;
            font-style: normal;
            font-weight: 600;
          }
        }
      }
    }
    .add_margin {
      margin-top: 43px;
      .game_box {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        align-items: center;
        width: calc(100% - 40px);
        margin: 0 auto;
        margin-top: 10px;
        .game_item {
          width: 33%;
          img {
            width: 100%;
            height:  auto;
          }
        }
      }
      .content_vip {
        width: calc(100% - 20px);
        margin-left: 20px;
        margin-top: 10px;
        position: relative;
        overflow-x: hidden;
         height: 266px;
         padding-top: 26px;
        .left {
          width: 238px;
          height: 182px;
          background: url("@/assets/home/vip_bg.png") no-repeat center;
          background-size: 100% 100%;
          position: relative;
          z-index: 2;
          
          .top_ttile {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding-top: 14px;
            box-sizing: border-box;
            img {
              width: 90px;
              height: 24px;
            }
            .sub {
              text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.50);
              font-family: PingFang SC;
              font-size: 16px;
              font-style: normal;
              font-weight: 400;
              background: linear-gradient(90deg, #FDE3AB 0%, #FFFDF8 50.5%, #FDE3AB 100%);
              background-clip: text;
              -webkit-background-clip: text;
              -webkit-text-fill-color: transparent;
              margin-top: -5px;
              span {
                background: linear-gradient(90deg, #FDE3AB 0%, #FFFDF8 50.5%, #FDE3AB 100%);
                background-clip: text;
                -webkit-background-clip: text;
                -webkit-text-fill-color: transparent;
                font-family: PingFang SC;
                font-size: 20px;
                font-style: normal;
                font-weight: 600;
                line-height: normal;
              }
            }
          }
          .middle_lists {
            width: 90%;
            margin: 0 auto;
            margin-top: 10px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            .middle_item {
              width: 32%;
              height: 36px;
              background: #FFE162;
              border-radius: 4px;
              margin-bottom: 5px;
              display: flex;
              align-items: center;
              justify-content: center;
              p {
                font-family: PingFang SC;
                font-size: 10px;
                font-style: normal;
                font-weight: 600;
                line-height: normal;
                background: linear-gradient(180deg, #FE1500 0%, #550700 100%);
                background-clip: text;
                -webkit-background-clip: text;
                -webkit-text-fill-color: transparent;
              }
            }
          }
          .bottom {
            display: flex;
            justify-content: center;
            margin-top: 4px;
            img {
              width: 74px;
              height: 21px;
            }
          }
        }
        .right {
          position: absolute;
          right: -40px;
          top: 0px;
          z-index: 3;
          img {
            width: 200px;
            height: 256px;
          }
        }
      }
    }
    .bottom_foot {
      position: fixed;
      left: 0;
      bottom: 0;
      height: 90px;
      background: #000;
      display: flex;
      justify-content: space-between;
      padding: 0 20px;
      box-sizing: border-box;
      align-items: center;
      gap: 12px;
      z-index: 999;
      .left {
        img {
          width: 61px;
          height: 61px;
        }
      }
      .right {
        img {
          width: 61px;
          height: 61px;
        }
      }
      .center {
        .first {
          color: #FFF;
          font-family: PingFang SC;
          font-size: 10px;
          font-style: normal;
          font-weight: 600;
          line-height: normal;
          opacity: 0.8;
          margin-bottom: 4px;
        }
        .sec {
          color: #FFF;
          font-family: PingFang SC;
          font-size: 20px;
          font-style: normal;
          font-weight: 600;
          line-height: normal;
          span {
            text-shadow: 0px 2px 4px #97541E;
            font-family: PingFang TC;
            font-size: 24px;
            font-style: normal;
            font-weight: 600;
            line-height: normal;
            letter-spacing: -0.72px;
            background: linear-gradient(180deg, #EDD084 20.59%, #FDF86A 48.13%, #EBC451 72.06%);
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
          }
        }
        .third {
          display: flex;
          align-items: center;
          margin-top: 4px;
          p {
            color: #FFF;
            font-family: PingFang SC;
            font-size: 10px;
            font-style: normal;
            font-weight: 500;
            line-height: normal;
            opacity: 0.8;
            margin-left: 4px;
          }
        }
      }
    }
    .servoce_box {
      position: fixed;
      right: 0;
      bottom: 200px;
      width: 71px;
      height: 75px;
      z-index: 999;
      img {
        width: 100%;
      }
    }
}

</style>
