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
          MGM is the world's most influential film promotion company,
          established in 1992, the main business: film promotion, theater
          cooperation, film stock. Entering the 21st century, as the film
          industry continues to boom, many profitable industries have gradually
          emerged, such as movie ticket sales or movie stocks. Before the 21st
          century, the sale of movie tickets and the qualification to buy movie
          stocks were in the hands of capitalists. When MGM entered the market
          and broke the monopoly, MGM expanded its ability to sell movie tickets
          to everyone, and split the movie stock into individual shares that
          everyone could buy. movie ticket center and movie stock exchange. MGM
          always believes that a person's power is limited, but if everyone
          works together, the power is unlimited.
        </p>
      </view>
    </view>
  </view>
</template>
<script>

export default {
  data() {
    return {
      title: "App Information",
    };
  },
  methods: {
    jumpHomePage() {
      uni.switchTab({
        url: "/pages/index/index",
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
  padding:15px 10px;
}
.left-btn img {
  width: 16px;
}
.main-title h3 {
  font-size: 16px;
  line-height: 20px;
}
.content{
  margin-top: 15px;
    width: 100%;
    padding: 0 25px;
}
.content p {
  font-size: 16px;
  line-height: 25px;
}
</style>
