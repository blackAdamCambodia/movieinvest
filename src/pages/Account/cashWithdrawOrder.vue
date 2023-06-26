<template>
    <view class="main">
      <view class="header">
        <view class="left_btn">
          <img @click="backAccount" src="../../static/back-arrow.png" alt="" />
        </view>
        <view class="Maintitle"><h3>{{title}}</h3></view>
        <view class="right_btn">
          <h3>Selective</h3>
        </view>
      </view>
      
    </view>
  </template>
  
  <script>
  export default {
    
    data() {
      return {
        title: "Withdrawal History",
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
    background: #fafafa;
    position: fixed;
    padding-top: 1.2rem;
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
    overflow-y: scroll;
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
    padding: 12px;
  }
  .left_btn img {
    width: 20px;
    height: 20px;
  }
  .Maintitle h3 {
    font-size: 16px;
    font-weight: 400;
  }
  .right_btn h3 {
    font-size: 12px;
  }
  


  </style>
  