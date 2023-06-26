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
                <h4>Real name</h4>
                <input type="text" placeholder="Enter your first and last name correctly">
            </li>
        </ul>
        <h3 v-if="!isInstall">Please enter you wallet address</h3>
        <view >
        <ul>
          <li>
              <h4>USDT-ERC20 address</h4>
              <input type="text" placeholder="Please enter USDT-ERC20 address">
          </li>
          <li>
              <h4>USDT-ERC20 address</h4>
              <input type="text" placeholder="please enter USDT-ERC20 address">
          </li>
        </ul>
        <ul v-if="!isInstall">
            <li class="withdrawal-password">
                <h4>Enter your withdrawal password</h4>
                <input type="text" placeholder="Enter a 4-digit password">                
            </li>
        </ul>
        <view v-if="!isInstall" class="agree">
          <view class="agree-top">
            <label>
						  <checkbox value="cb" checked="true"  style="transform:scale(0.7)" />I agree to the 'Service agreement'
					  </label>            
          </view>
          <view class="agree-bottom">
            <p> Members note: in order not to be affected to your withdrawal process, please make sure to enter your real name and correct receiving wallet address, remember your withdrawal password</p>
          </view>

        </view>
      </view>
      </view>
      
      <view class="information">
        <p v-if="isInstall" class="informationText">Hot source. please fill in the correct wallet address to ensure the success of the withdrawal thank you !</p>
        <button v-if="isInstall" @click="hideInformationBtn" class="informationBtn" type="button">Install information now</button>
      </view>
      <button v-if="!isInstall" type="button">Confirm Link</button>
    </view>
  </template>
  
  <script >
    
  export default {
    
    data() {
      return {
        title: "Link wallet address",
        isInstall:true
      };
    },
    methods: {
    hideInformationBtn() {
      this.isInstall = false;       
    },
    backAccount(){
      uni.navigateBack({
        url: '/pages/Account/myaccount'
      });
    }
    }
  };
  </script>
  
  <style scoped>
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
    overflow-x: scroll;
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
    padding:20px 0 10px;
    background: #fff;
  }
  .password-reset ul li {
    list-style: none;
    padding: 0 15px;
  }
  .password-reset ul li h4 {
    font-size: 14px;
    padding: 14px 0;
    color: #000;
    font-weight: 400;
    
  }
  .password-reset ul li input {
    border: 1px solid #ddd;
    color:#666;
    border-radius: 6px;
    height: 40px;
    width: 90%;
    padding: 0 10px;
    font-size: 14px;
  }
  .password-reset h3 {
    padding: 14px 8px;
    background-color: #eee;
    font-size: 15px;
    line-height: 1rem;
    color: #333;
    margin-top: 10px;
    font-weight: 400;
  }
 
  .withdrawal-password h4 {
    width: 200px;
    line-height: 30px;  
  }
  button {
    background: #2f3848;
    color: #fff;
    width: 90%;
    display: block;
    margin: 30px auto;
   
  }
  .agree {
    padding: 0 15px;
  }
  .agree-top {
    display: flex;
    padding: 15px 0;
  }
  .agree-bottom p {
    font-size: 12px;
    line-height: 16px;
    color: #2f3848;
   
  }
  .information p {
    font-size: 9px;
    padding: 0 15px;
  }
  .informationBtn,
  .informationText{
    display: block;
  }

  </style>
  