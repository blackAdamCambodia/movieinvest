<template>
    <view class="content">
        <view class="title">
            <text >{{ title }}</text>
        </view>
        <view class="customer-support">
            <image class="profileImage" src="/static/profile-image.png"></image>
            <p>Hi, You are my exclusive customer</p>
        </view>
        <view class="online-service">
            <h3>Online Customer Service</h3>

        </view>
      
      
    </view>
  </template>  
  <script>    
  export default {  
   data() {
      return {
        title: "Customer",
        
      };
    },
    onLoad() {},
    methods: {},
  };
  </script>
  
  <style>
    .content {
      background: rgb(242, 242, 242);
      height: 100vh;
    }
  .title {
    text-align: center;
    font-size: 16px;
    padding: 12px 0;
  }
  .customer-support {
    height: 80px;
    display: flex;
    align-items: center;
    padding: 0 0.26667rem;
    background: url(../../static/customer-support-background.png) no-repeat;
    background-size: 100%;
    
  }
 .customer-support image {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  margin-left: 10px;
}
.customer-support p {
  color: #fff;
  margin-left: 10px;
  font-size: 16px;
}
.online-service {
  background: #fff;
    padding: 5px 14px 0px 0px;
    border-bottom-left-radius: 8px;
    border-bottom-right-radius: 8px;
}
.online-service h3 {
  margin-top: 40px;
  border-radius: 0.26667rem;
    background: #fff url(../../static/online-customer-service-bg.png) no-repeat;
    background-size: 100%;
    height: 100px;
    margin-bottom: 0.4rem;
    padding: 15px 15px 0;
    font-size: 18px;
    font-weight: 700;
}

  </style>
  