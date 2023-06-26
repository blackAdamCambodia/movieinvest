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
      <view class="nav">
        
        <u-subsection :list="list"
					mode="button"
					:current="current"
					activeColor="#007aff"
					@change="change">
        </u-subsection>
      </view>
      <view class="con">
        <view>
            <p>No figures available</p>
        </view>
      </view>
    </view>
  </template>
  
  <script>
  export default {
    
    data() {
      return {
        title: "Loading History",
        list: ['Recharge offline', 'Recharge online'],
				current: 1
      };
    },
    methods: {
      change(index) {
				this.current = index
			},
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
    padding: 15px 12px;
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
  .nav {
    overflow: hidden;
    border-radius: 10px 10px 0px 0px;
    background-color: #fff;
    display: flex;
    align-items: center;
    padding: 12px 0;
    margin-top: 15px;
  }
  .__avatar {
			background-color: #fff;
			
		}
.u-subsection--button {
    text-align: center;
    color: #333;
    
    height: 48px;
    line-height: 40px;
    display: flex;
    justify-content: space-around;
    background: #fff !important;
    box-shadow: 0 0 1px #b8bbbf;
    border: 0;
    border-radius: 4px;
    cursor: pointer;
    padding: 27px 0;
  }

.con {
    
    height: 48px;
    text-align: center;
    margin-top: 1px;
}


.con p {
    font-size: 10px;
    line-height: 1.46667rem;
    text-align: center;
    color: #919191;
   background: #fff;
    padding: 12px;
   
    outline: 0;
}

  </style>
  