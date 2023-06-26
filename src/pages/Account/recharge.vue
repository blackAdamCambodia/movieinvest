<template>
  <view class="main">
    <view class="header">
      <view class="left_btn">
        <img @click="backAccount" src="../../static/back-arrow.png" alt="" />
      </view>
      <view class="Maintitle"><h3>{{title}}</h3></view>
      <view class="right_btn">
        <h3>History</h3>
      </view>
    </view>
    <view class="deposit-details">
      <view class="deposit-title">
        <h3>Deposit amount</h3>
      </view>
      <view class="deposit-amount">
        <span>$</span>
        <input 
          placeholder="Please enter the amount to deposit"
          type="text"
        />
      </view>
    </view>
    <view class="customer-service">
      <h3>Please select a recharge channel</h3>
      <view class="service-to-recharge">
        <view class="support-img">
          <img src="../../static/support-img.png" alt="" />
        </view>
        <view class="support-title">
          <h4>Multilingual Customer Service</h4>
          <p>Contact customer service to recharge</p>
        </view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  
  data() {
    return {
      title: "Recharge management",
    };
  },
  methods: {
    backAccount(){
      uni.navigateBack({
        url: '/pages/Account/myaccount'
      });
    }
  }
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Montserrat", sans-serif;
}
.main {
  padding: 10px;
  background: #fff;
  position: fixed;
  padding-top: 1.2rem;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
 
}
.header {
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
  background: #fff;
  color: #464646 !important;
  font-size: 15px;
  z-index: 99999999;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 10px;
}
.left_btn img {
  width: 16px;
 
}
.Maintitle h3 {
  font-size: 16px;
  font-weight: 400;
}
.right_btn h3 {
  font-size: 12px;
  font-weight: 400;
}
.deposit-details {
  background: #fff;
  box-shadow: 0 2px 8px 3px rgba(0, 0, 0, 0.1);
  border-radius: 6px;
  margin-bottom: 6px;
  padding: 15px;
  margin-top: 43px;
}
.deposit-title h3 {
    font-size: 16px;
    margin-bottom: 20px;
    font-weight: 400;
}
.deposit-amount {
  border-bottom: 2px solid #e3e6ee;
  line-height: 30px;
  display: flex;
}
.deposit-amount span {
  font-size: 20px;
  font-weight: 800;
}
.deposit-amount input {
  border: none;
  color: #000;
  border: none;
  padding: 0;
  background: none;

  font-size: 18px;
  margin-left: 5px;
  width: 100%;
}
.customer-service h3 {
  font-size: 18px;
  line-height: 14px;
  color: #333;
  margin-top: 24px;
  font-weight: 500;
  margin-bottom: 10px;
  padding:0 15px;
}
.service-to-recharge {
  overflow: hidden;
  padding: 10px 0;
  background: url(../../static/support-bg.png) no-repeat 0 0;
  background-size: 100% 100%;
  height: 140px;
  background-origin: content-box;
  background-color: #fff;
  position: relative;
  border-radius: 10px;
  display: flex;
}
.support-img {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  margin: 10px 10px 0 15px;
}
.support-img img {
  width: 100%;
}

.support-title h4 {
  color: #fff;
  font-size: 18px;
  margin-top: 15px;
  margin-bottom: 20px;
  font-weight: 400;
}
.support-title p {
  font-size: 12px;
  color: #fff;
}
</style>
