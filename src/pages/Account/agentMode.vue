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
        <p>
          According to statistics in January 2022, MGM has a total of 1 billion
          dealers in many countries around the world. In order to better serve
          dealers, the group has shifted its business from offline stores to
          online APP to help agents buy movies online Tickets move. Telephone.
          The sale and purchase of film stock. When you become an agent of MGM,
          you can enjoy the support of opening the group's outlet stores and the
          support of opening movie theaters. For specific support plan, please
          contact customer service of MGM platform for consultation. Customer
          service lines have been opened in 50 countries, and each country has
          an independent APP service center. Agents provide the highest quality
          service.
        </p>
      </view>
    </view>
  </view>
</template>
<script>
export default {
  data() {
    return {
      title: "Agent Mode",
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
