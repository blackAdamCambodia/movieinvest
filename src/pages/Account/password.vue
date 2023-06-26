<template>
    <view class="main">
      <view class="header">
        <view class="left_btn">
          <img @click="backAccount" src="../../static/back-arrow.png" alt="" />
        </view>
        <view class="Maintitle"><h3>{{title}}</h3></view>
        <view class="right_btn"></view>
      </view>
      <view class="password-reset">
        <ul>
            <li>
                <h4>Password</h4>
                <input type="text" placeholder="Enter your Password">
            </li>
            <li>
                <h4>Confirm Password</h4>
                <input type="text" placeholder="Please Re-enter your Password">
            </li>
        </ul>
        <h3>Withdrawal Password</h3>
        <view >
        <ul>
            <li class="withdrawal-password">
                <h4>Enter your withdrawal password</h4>
                <input type="password">
                <input type="password">
                <input type="password">
                <input type="password">
            </li>
        </ul>
      </view>
      </view>
      
      
      <button type="button">Confirm</button>
    </view>
  </template>
  
  <script>
  export default {
    
    data() {
      return {
        title: "Password Manager",
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
    background: #fff;
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
  .password-reset {
    padding:30px 0 10px;
    background: #fff;
  }
  .password-reset ul li {
    list-style: none;
    
    padding: 0 15px;
  }
  .password-reset ul li h4 {
    font-size: 15px;
    padding: 14px 0;
    color: #000;
    font-weight: 400;
    
  }
  .password-reset ul li input {
    border: 1px solid #ddd;
    color:#666;
    border-radius: 6px;
    height: 35px;
    width: 80%;
    padding: 0 10px;

  }
  .password-reset h3 {
    padding: 14px 8px;
    background-color: #eee;
    font-size: 13px;
    line-height: 1rem;
    color: #333;
    margin-top: 10px;
    font-weight: 400;
  }
  .withdrawal-password {
    display: flex;
    
  }
  .withdrawal-password input {
    max-width: 35px;
    margin-top: 8px;
  }
  .withdrawal-password h4 {
    width: 200px;
    line-height: 40px;
    padding: 0 !important;
    
  }
  button {
    background: #2f3848;
    color: #fff;
    width: 90%;
    display: block;
    margin: 0 auto;
    margin-top: 40px;
  }
  </style>
  