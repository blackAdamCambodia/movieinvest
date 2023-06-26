<template>
  <view class="main">
    <view class="header">
      <view class="left_btn">
        <img @click="backAccount" src="../../static/back-arrow.png" alt="" />
      </view>
      <view class="Maintitle"
        ><h3>{{ title }}</h3></view
      >
      <view class="right_btn"></view>
    </view>
    <view class="notice">
      <img src="../../static/notification-bg.png" alt="" />
    </view>
    <view class="notice-ul">
      <li>
        <view class="Notice_ul_left">
          <img src="../../static/bell-icon.png" alt="" />
        </view>
        <h3>Notice</h3>
      </li>
      <view>
        <p class="no-more-figure">No figures available</p>
      </view>
    </view>
   
  </view>
</template>

<script>
export default {
  data() {
    return {
      title: "Notification",
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
    width: 16px;
    height: 15px;
  }
.notice {
  width: 100%;
}
.notice img {
  width: 100%;
  height: 200px;
}
.notice-ul {
    width: 90%;
    border-radius: 8px;
    padding: 40px 15px;
    background-image: linear-gradient(#f8f4f4,#fff);
    position: relative;
    top: -30px;
    left: 5%;
}
.notice-ul li {
    list-style: none;
    overflow: hidden;
    display: flex;
    align-items: center;
    border-radius: 8px;
    margin-bottom: 10px;
    padding:10px 15px;
    background: #fff url(../../static/right-arrow-icon.png) no-repeat 100%;
    background-size: auto 15px;
    background-origin: content-box;
    box-shadow: 0 5px 8px rgba(0,0,0,.1);
}
.Notice_ul_left {
    padding-right:  5px ;
    border-right: 1px solid #eee ;
    margin-right: 10px;
}
.Notice_ul_left img {
    width: 25px;
    height: 25px;
    margin-right: 10px;
}
.no-more-figure {
    font-size: 10px;
    text-align: center;
    color:#919191;
    margin-top: 20px;
}
</style>
