<template>
  <view>
    <view class="main-content">
        <view class="header-title">
            <h2>{{ title }}</h2>
        </view>
      <view class="ad">
        <view class="banner-part">
            <img src="../../static/home-banner.png" alt="">
        </view>    
        <view class="animation-text">
                <u-icon class="speaker-icon"  name="volume" color="#ffffff" size="18"></u-icon>
                <marquee width="80%" direction="left" height="100px">
                    online.Thank you!Hello MGM users!At the request of the International Film Management Center, starting from June 4, 2023, the MGM platform system update time will be adjusted to: 00:00 US Eastern Time&amp;nbsp;From June 5, 2023, the customer service hours of the MGM platform will be adjusted to: 24 hours
                </marquee>
        </view>
        <view class="feature">
            <view @click="jumpMoviePage" class="movie">
                    <img src="../../static/movie-folder-icon.png" alt="">
                    <p>Movie</p>
            </view>
            <view @click="jumpRechargePage" class="recharge">
                    <img src="../../static/recharge-icon.png" alt="">
                    <p>Recharge</p>
            </view>
            <view @click="jumpWithdrawPage" class="withdraw">
                    <img src="../../static/withdraw-icon.png" alt="">
                    <p>Withdraw</p>
            </view>
            <view @click="jumpWithdrawHistory" class="withdraw-history">
                    <img src="../../static/withdraw-history-icon.png" alt="">
                    <p>Withdraw History</p>
            </view>               
        </view>
      </view>
      <view class="quest-corridor">
            <view class="quest-title">
                <img src="../../static/quest-icon.png" alt="">
                <p>Quest Corridor</p>
            </view>
            <view>
              <view class="announcement-task">
                <ul>
                    <li class="announcement vipOneBg">
                        <view class="user">
                            <view class="info">
                               <h3>
                                LV1
                               </h3> 
                            </view>
                            <view class="pic">
                                <img src="../../static/vip-icon.png" alt="">
                                 <i></i>
                            </view>
                        </view>
                        <view class="entry-fee">
                            <p>
                                Enter $100 <br> 0.30%｜30In turn 
                            </p>
                        </view>
                        <view class="right">
                            <p>Enter</p>
                        </view>
                    </li>
                    <li class="announcement vipTwoBg">
                        <view class="user">
                            <view class="info">
                               <h3>
                                LV2
                               </h3> 
                            </view>
                            <view class="pic">
                                <img src="../../static/vip2-icon.png" alt="">
                                 <i></i>
                            </view>
                        </view>
                        <view class="entry-fee">
                            <p>
                                Enter $100 <br> 0.30%｜30In turn 
                            </p>
                        </view>
                        <view class="right">
                            <p>Enter</p>
                        </view>
                    </li>
                    <li class="announcement vipThreeBg">
                        <view class="user">
                            <view class="info">
                               <h3>
                                LV3
                               </h3> 
                            </view>
                            <view class="pic">
                                <img src="../../static/vip3-icon.png" alt="">
                                 <i></i>
                            </view>
                        </view>
                        <view class="entry-fee">
                            <p>
                                Enter $100 <br> 0.30%｜30In turn 
                            </p>
                        </view>
                        <view class="right">
                            <p>Enter</p>
                        </view>
                    </li>
                    <li class="announcement vipfourBg">
                        <view class="user">
                            <view class="info">
                               <h3>
                                LV4
                               </h3> 
                            </view>
                            <view class="pic">
                                <img src="../../static/vip4-icon.png" alt="">
                                 <i></i>
                            </view>
                        </view>
                        <view class="entry-fee">
                            <p>
                                Enter $100 <br> 0.30%｜30In turn 
                            </p>
                        </view>
                        <view class="right">
                            <p>Enter</p>
                        </view>
                    </li>
                    <li class="announcement vipFiveBg">
                        <view class="user">
                            <view class="info">
                               <h3>
                                LV5
                               </h3> 
                            </view>
                            <view class="pic">
                                <img src="../../static/vip5-icon.png" alt="">
                                 <i></i>
                            </view>
                        </view>
                        <view class="entry-fee">
                            <p>
                                Enter $100 <br> 0.30%｜30In turn 
                            </p>
                        </view>
                        <view class="right">
                            <p>Enter</p>
                        </view>
                    </li>
                    <li class="announcement VipSixBg">
                        <view class="user">
                            <view class="info">
                               <h3>
                                LV6
                               </h3> 
                            </view>
                            <view class="pic">
                                <img src="../../static/vip6-icon.png" alt="">
                                 <i></i>
                            </view>
                        </view>
                        <view class="entry-fee">
                            <p>
                                Enter $100 <br> 0.30%｜30In turn 
                            </p>
                        </view>
                        <view class="right">
                            <p>Enter</p>
                        </view>
                    </li>
                </ul>
            </view>
            </view>
        </view>
        <view class="stable-content">
            <view class="stable-title">
                <h3>MGM</h3>
                <p>Professional and stable</p>
            </view>
            <view class="professional-list">
                <ul>
                    <li @click="jumpInfomation">
                        <img src="../../static/lnformation-icon.png" alt="">
                    </li>
                    <li @click="jumpAgentMode">
                        <img src="../../static/Agentmode.png" alt="">
                    </li>
                    <li @click="jumpVipOffer">
                        <img src="../../static/vip-offer.png" alt="">
                   </li>
                </ul>
            </view>
            <view class="prize">
                <view class="active-member-title">
                    <h3>Active member</h3>
                </view>
                <view class="con">
                    <ul class="anim">
                        <li>
                            <img src="../../static/mgm-icon.png" alt="">
                            <view class="id-details">
                                <h3 class="id">ID:840**56</h3>
                                <p class="date">19/16/23</p>
                            </view>
                            <h4>Profit</h4>
                            <span>
                                90000$
                            </span>
                        </li>
                        <li>
                            <img src="../../static/mgm-icon.png" alt="">
                            <view class="id-details">
                                <h3 class="id">ID:842**94</h3>
                                <p class="date">19/16/23</p>
                            </view>
                            <h4>Profit</h4>
                            <span>
                                80000$
                            </span>
                        </li>
                        <li>
                            <img src="../../static/mgm-icon.png" alt="">
                            <view class="id-details">
                                <h3 class="id">ID:980**51</h3>
                                <p class="date">19/16/23</p>
                            </view>
                            <h4>Profit</h4>
                            <span>
                                60000$
                            </span>
                        </li>
                    </ul>
                </view>
                <view class="flim-company">
                    <img src="../../static/footer-image.png" alt="">
                </view>
            </view>
            
        </view>     
    </view>
    </view>     
</template>
<script>
import Information from "../Account/information.vue";
export default {
    components: { Information },
    data() {
      return {
        title: "Home Page",
        
      };
    },
    methods: {
        jumpMoviePage(){
        uni.switchTab({
        url: '/pages/Movie/movie'
      });
    },
    jumpRechargePage(){
        uni.navigateTo({
        url: '/pages/Account/recharge'
      });
    },
    jumpWithdrawPage(){
        uni.navigateTo({
        url: '/pages/Account/cash'
      });
    },
    jumpWithdrawHistory(){
        uni.navigateTo({
        url: '/pages/Account/cashWithdrawOrder'
      });
    },
    jumpInfomation(){
        uni.navigateTo({
        url: '/pages/Account/information'
      });
    },
    jumpAgentMode(){
        uni.navigateTo({
        url: '/pages/Account/agentMode'
      });
    },
    jumpVipOffer(){
        uni.navigateTo({
        url: '/pages/Account/vipOffer'
      });
    }
    }  
}
</script>
<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Montserrat', sans-serif;
} 
.main-content {
    border-bottom: 2rem solid #f1f1f1;
    background: linear-gradient(180deg,#e22a2a,#fff);
    background-size: 100% 25%;
    background-repeat: no-repeat;
    padding-top: 20px;
    overflow: scroll;
}
.header-title {
    width: 100%;
    position: fixed;
    top: 0;
    left: 0;
    background: #e54847;
    padding: 14px 0;
    z-index: 99999999;

}
.header-title h2 {
    line-height: 22px;
    text-align: center;
    color: #fff;
    font-size: 16px;
    font-weight: 600;
}
.banner-part {
    width: 100%;
    margin: 0 auto;
}
.banner-part img {
    width: 100%;
    margin-top: 40px;
    border-radius: 8px;
}

.animation-text {
    
    background: rgba(245, 108, 108, 0.6);
    margin-top: 4.2667px;
    height: 40px;
    padding: 0 40px;
    font-size: 14px;
    line-height: 30px;
    margin-bottom: 10px;
    display: flex;
    align-items: center;
    overflow: hidden;
    position: relative;
    
}
.speaker-icon {
    max-width: 24px; 
    display: inline-block;
    position: relative;
    margin-left: -25px;
}
marquee {
    position: absolute;
    top: 5px;
    overflow: hidden;
    color: white;
}
.feature {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: #fff;
    padding: 10px 0;
    margin-bottom: 15px;
}
.movie img,
.recharge img, 
.withdraw img,
.withdraw-history img {
    width: 50px;
    aspect-ratio: auto 50 / 50;
    height: 50px;
}
.movie,
.recharge, 
.withdraw,
.withdraw-history {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100%;
    width: 100%;
}

.movie p,
.recharge p, 
.withdraw p,
.withdraw-history p {
    color: #646566;
    font-size: 12px;
    line-height: 1.5;
     font-weight: 600;
} 
.ad {
    border-bottom: 5px solid #f2f2f2;
    padding: 0 15px;
}
.quest-corridor
 {
    padding: 0 15px; 
}
.quest-title {
    display: flex;
    gap: 15px;
    padding: 10px 0 15px;
}
.quest-title p {
    font-size: 16px;
    font-weight: 700;    
}
.announcement-task ul {
    
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
}
.announcement-task ul li {
    width: 100%;
    height: 100px;
    padding:10px 30px;
    background: #5d7498 url(../../static/vip-card.png) no-repeat;
    background-size: 30%;
    margin-bottom: 10px;
    border-radius: 10px;
    background-position: 50%;
    padding-left: 80px;
    list-style: none;
}
.vipTwoBg {
    background-color: #e78118 !important;
}
.vipThreeBg {
    background-color: #2b3b94 !important;
}
.vipfourBg {
    background-color: #3aa1a5 !important;
}
.vipFiveBg {
    background-color: #2c2e32 !important;
}
.VipSixBg {
    background-color: #51029c !important;
}
.announcement-task ul li .user {
    display: flex;
    justify-content: space-between;
}
.announcement-task ul li .user .info h3 {
    font-size: 28px;
    color: #fff;
    font-weight: 700;
    margin-bottom: 5px;
}
.announcement-task ul li .user .pic {
    width: 50px;
    height: 50px;
    border-radius: 5px;
    overflow: hidden;
    position: absolute;
    margin-left: 10px;
    animation: updown 1s infinite;
    left: 20px;
    margin-top: 10px;
   
}
@keyframes updown {
    0% {
        transform: translateY(14px)
    }

    50% {
        transform: translateY(0)
    }

    to {
        transform: translateY(14px)
    }
    
  }
  .announcement-task ul li .user .pic i {
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    background: rgba(0,0,0,.5) url(../../static/lock-icon.png) no-repeat 50%;
    background-size: 16px;
}

.announcement-task ul li .user .pic img {
    width: 100%;
}
.entry-fee p {
    font-size: 12px;
    color: #fff;
}
.announcement-task ul li .right {
    position: absolute;
    right: 30px;
    z-index: 999;
    margin-top: -70px;
    color: #fff;
    font-size: 15px;
    font-weight: 700;
}
.stable-title h3 {
    font-size: 25px;
    font-weight: 700;
    background: url(../../static/stableBg.png) no-repeat 50%;
    background-size: 50%;
    text-align: center;
}
.stable-title p {
    font-size: 15px;
    color: #696051;
    text-align: center;
}
.professional-list {
    margin: 20px auto;
}
.professional-list ul {
    display: flex;
    justify-content: space-around;
    align-items: center;
}
.professional-list ul li {
    width: 60px;
    list-style: none;
}
.professional-list ul li img {
    width: 100%;
}
.prize {
    padding: 0 15px;
    padding-bottom: 15px;
}

.active-member-title {
    padding: 10px 0;
}
.active-member-title h3 {
    font-size: 22px;
}
.con ul {
    border-radius: 6px;
    box-shadow:-3px 2px 9px 0 rgba(0,0,0,.15);
    background: #fff;
    list-style: none;
}
.con ul li {
    display: flex;
    padding: 14px 10px;
    align-items: center;
    justify-content: space-around;
}
.con ul li img {
    width: 50px;
}
.id-details h3 {
    font-size: 16px;
    color: #333;
    font-weight: 700;
} 
.id-details p {
    font-size: 14px;
    color: #555;
    margin-top: 5px;
}
.con h4 {
font-size: 18px;
font-weight: 400;
}
.con ul li span {
    font-size: 13px;
    color: #ff9200;
    background: #fff7ce;
    background-size: 0.53333rem;
    line-height: .72rem;
    border-radius: 8px 0 8px 0;
    padding: 8px 6px 8px 10px;
}
.flim-company {
    padding-top: 10px;
    
}
.flim-company img {
    width: 100%;
}


</style>