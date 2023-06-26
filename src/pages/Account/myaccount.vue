<template>
  <view>
    <view class="main-content">
      <view class="header-title">
        <h2>{{ title }}</h2>
      </view>
      <view class="user">
        <view>
          <view class="user-details">
            <h3>62-845694686</h3>
            <view  class="user-level">
                <img
             src="../../static/user-level.webp"
             mode="scaleToFill"
           />
            </view>
           
          </view>
          <p class="user-id">ID:96148</p>
        </view>
        <image class="logo" src="/static/mgm-logo.png"></image>
      </view>
      <view class="balance">
        <view class="balance-header">
          <view>
            <img src="../../static/doller-icon.png" alt="" />
          </view>
          <view>
            <h3>My assets</h3>
          </view>
          <view></view>
        </view>
        <view>
          <ul class="balance-details">
            <li class="balance-amount">
              <h3>Available balances</h3>
              <p>0.00</p>
            </li>
            <li class="profit-amount">
              <h3>Profit of the day</h3>
              <p>0.00</p>
            </li>
          </ul>
        </view>
      </view>
      <view class="nav">
        <view class="button" @click="jumpRecharge">
            <view class="nav-icon">
                <img src="../../static/recharge-image.png" alt="">
                <p>Recharge</p>
            </view>
            <img class="font-arrow" src="../../static/arrow-back-icon.png" alt="">
        </view>
        <view class="button"  @click="jumpWithdraw">
            <view class="nav-icon">
                <img src="../../static/withdraw-img.png" alt="">
                <p>Withdraw</p>
            </view>
            <img class="font-arrow" src="../../static/arrow-back-icon.png" alt="">
        </view>
        <view class="button" @click="jumpLoading" >
            <view class="nav-icon">
                <img src="../../static/loding-img.png" alt="">
                <p>Loding history</p>
            </view>
            <img class="font-arrow" src="../../static/arrow-back-icon.png" alt="">
        </view>
        <view class="button" @click="jumpCashWithdraw">
            <view class="nav-icon">
                <img src="../../static/withdraw-history-img.png" alt="">
                <p>Withdrawal history</p>
            </view>
            <img class="font-arrow" src="../../static/arrow-back-icon.png" alt="">
        </view>
        <view class="button" @click="jumpPassword">
            <view class="nav-icon">
                <img src="../../static/password-img.png" alt="">
                <p>Password Manager</p>
            </view>
            <img class="font-arrow" src="../../static/arrow-back-icon.png" alt="">
        </view>
        <view class="button" @click="jumpBankCard">
            <view class="nav-icon">
                <img src="../../static/bank-card-img.png" alt="">
                <p>Bank Card Management</p>
            </view>
            <img class="font-arrow" src="../../static/arrow-back-icon.png" alt="">
        </view>
        <view class="button" @click="jumpNotification">
            <view class="nav-icon">
                <img src="../../static/notification-img.png" alt="">
                <p>Notification</p>
            </view>
            <img class="font-arrow" src="../../static/arrow-back-icon.png" alt="">
        </view>
        <view class="button" @click="jumpTeam">
            <view class="nav-icon">
                <img src="../../static/team-img.png" alt="">
                <p>Team</p>
            </view>
            <img class="font-arrow" src="../../static/arrow-back-icon.png" alt="">
        </view>
        <view class="button" @click="jumpBankCard">
            <view class="nav-icon">
                <img src="../../static/bank-card-management.png" alt="">
                <p>Bank Card Management</p>
            </view>
            <img class="font-arrow" src="../../static/arrow-back-icon.png" alt="">
        </view>
      </view>
      <view>
        <button @click="loginPage" type="button" class="exit-btn">Exit</button>
      </view>
    </view>
  </view>
</template>
<script>

export default {
  
  data() {
    return {
      title: "Individual",
    };
  },
  methods: {
    jumpRecharge(){
      uni.navigateTo({
        url: '/pages/Account/recharge'
      });
    },
    jumpWithdraw(){
      uni.navigateTo({
        url: '/pages/Account/cash'
      });
    },
    jumpLoading(){
      uni.navigateTo({
        url: '/pages/Account/loadinghistory'
      });
    },
    jumpCashWithdraw(){
      uni.navigateTo({
        url: '/pages/Account/cashWithdrawOrder'
      });
    },
    jumpPassword(){
      uni.navigateTo({
        url: '/pages/Account/password'
      });
    },
    jumpBankCard(){
      uni.navigateTo({
        url: '/pages/Account/BindCard'
      });
    },
    jumpNotification(){
      uni.navigateTo({
        url: '/pages/Account/informationNotice'
      });
    },   
    jumpTeam(){
      uni.navigateTo({
        url: '/pages/Account/teamList'
      });
    },
    jumpBankCard(){
      uni.navigateTo({
        url: '/pages/Account/BindCard'
      });
    },
    loginPage(){
      uni.navigateTo({
        url: '/pages/Account/login'
      });
    }
  },
};
</script>
<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Montserrat", sans-serif;
}
.main-content {
 
  background: linear-gradient(180deg, #e22a2a, #fff);
  background-size: 100% 50%; 
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
.logo {
  height: 80px;
  width: 80px;

  border-radius: 50%;
  animation: rotateImage 10s linear infinite;
}
@keyframes rotateImage {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
.user {
  display: flex;
  justify-content: space-between;
  align-items: start;
  margin-top: 30px;
  padding: 5px 15px;
}
.user-details {
  display: flex;
  justify-content: space-between;
  align-items: start;
}
.user-level {
  width: 50px;
  height: 22px;
}
.user-level img {
    width: 100%;
    height: 100%;
}
.user-details h3 {
  color: #fff;
  margin-right: 10px;
  font-size: 16px;
}
.user-id {
  font-size: 12px;
  color: #fff;
  margin-top: 20px;
}
.balance {
    background: #fff;
    border-radius: 10px;
    box-shadow: 0 .64px 2.1333px 0 rgba(0,0,0,.15);
    margin: 0 12px;
    padding: 18px 12px 25px;
}
.balance-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 15px;
}
.balance-header img {
    width: 25px;
}
.balance-header h3 {
    font-size: 14px;
    font-weight: 700;
}
.balance-details {
    display: flex;
    justify-content: space-between;
    list-style: none;
    gap: 5px;
    
}
.balance-amount {
  width: 100%;
    height: 100%;
    padding: 14px 10px; 
    background: url(../../static/balance-bg.png) no-repeat;
    background-size: 100% 100%;
}
.profit-amount {
    width: 100%;
    height: 100%;
    padding: 14px 10px; 
    background: url(../../static/profit-bg.png) no-repeat;
    background-size: 100% 100%;
    
}
.balance-amount h3,
.profit-amount h3 {
    font-size: .62rem;
    color: #878f9a;
    padding: 8px ;
}
.balance-amount p,
.profit-amount p {
    font-size: 1.125rem;
    font-weight: 700;
    color: #000;
    padding: 0 0 0 10px ;
}
.nav {
    background: #fff;
    padding: 20px 16px 0;
    border-radius:8px;
    box-shadow: 0 0.04rem 0.13333rem 0 rgba(0,0,0,.15);
    margin: 10px;
}
.button {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 12px 0;
}
.button::after {
    position: absolute;
    box-sizing: border-box;
    content: " ";
    pointer-events: none;
    right: 16px;
    left: 16px;
    border-bottom: 1px solid #ebedf0;
    -webkit-transform: scaleY(.5);
    transform: scaleY(.5);
    width: 320px;
    margin: 0 auto;
    margin-top: 50px;
}
.button::after:last-child {
    border-bottom:0
}
.nav-icon {
    display: flex;
    gap: 10px;
    align-items: center;
}
.nav-icon img {
    width: 30px;
    height: 30px;
}
.font-arrow {
    transform: rotate(180deg);
    width: 14px;
    height: 14px;
    margin-right: 10px;
}
.exit-btn {
    color: white;
    background: linear-gradient(to right, rgb(255, 96, 52), rgb(238, 10, 36));
    border: 0px;
    font-size: 14px;
    border-radius:0 ;
    margin: 10px;
    margin-bottom: 10px;
    padding: 5px 0;
}
</style>
