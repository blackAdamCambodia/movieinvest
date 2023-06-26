<template>
  <view>
    <view class="main">
      <view class="header">
        <view @click="jumpHomePage" class="left-btn">
          <img src="../../static/arrow-back-icon.png" alt="" />
        </view>
        <view class="main-title">
          <h3>{{ title }}</h3>
        </view>
        <view class="right-btn"></view>
      </view>
      <view class="content">
        <span>
          <p>LV1 $ 100 30 push tickets, salary income 0.30%</p>
          <p>LV2 $ 1000 50 push tickets, salary income 0.31%</p>
          <p>LV3 3000$ 60 push tickets, salary income0.33%</p>
          <p>LV4 5000$ 70 push tickets, salary income0.35%</p>
          <p>LV5 10000$ 80 push tickets, salary income 0.37%</p>
          <p>LV6 20000$ 90 push tickets, salary income 0.40%</p>
        </span>
      </view>
    </view>
  </view>
</template>
<script>
export default {
  data() {
    return {
      title: "Vip Offer",
    };
  },
  methods: {
    jumpHomePage() {
      uni.switchTab({
        url: "/pages/index/index",
      });
    },
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
.main {
  background-color: #fff;
  min-height: 100vh;
  overflow-y: scroll;
  overflow-x: hidden;
  margin-top: 40px;
}

.header {
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
  background: #fff;
  color: #464646 !important;
  font-size: 0.37333rem;
  z-index: 99999999;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 10px;
}
.left-btn img {
  width: 16px;
}
.main-title h3 {
  font-size: 16px;
  line-height: 20px;
}
.content {
  margin-top: 15px;
  width: 100%;
  padding: 0 25px;
}
.content p {
  font-size: 16px;
  line-height: 25px;
}
</style>
