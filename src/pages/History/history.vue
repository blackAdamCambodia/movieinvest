<template>
  <view class="main">
    <view class="header">
      <view class="left-btn">
        <img
          @click="jumpHomePage"
          src="../../static/arrow-back-icon.png"
          alt=""
        />
      </view>
      <view class="main-title">
        <h3>{{ title }}</h3>
      </view>
      <view class="right-btn"></view>
    </view>
    <view class="recodes">
      <view class="sub-menu">
        <u-tabs
          class="sub-navbar"
          :list="list4"
          lineWidth="24"
          lineColor="#f56c6c"
          :activeStyle="{
            color: '#303133',
            fontWeight: 'bold',
            transform: 'scale(1.05)',
          }"
          :inactiveStyle="{
            color: '#606266',
            transform: 'scale(1)',
          }"
          itemStyle="padding-left: 15px; padding-right: 15px; height: 34px;"
        >
        </u-tabs>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      title: "Quest History",

      list4: [
        {
          name: "Total",
        },
        {
          name: "In Process",
        },
        {
          name: "Done",
        },
        {
          name: "Freeze",
        },
      ],
    };
  },
  methods: {
    jumpHomePage() {
      uni.switchTab({
        url: "/pages/index/index",
      });
    },
    setActiveTab(tabName) {
      this.activeTab = tabName;
    },
  },
};
</script>

<style>
.main {
  width: 100%;
  height: 100%;
  position: fixed;
  top: 0;
  left: 0;
  overflow-y: scroll;
  background: #f1f1f1;
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
  padding: 10px;
}
.left-btn img {
  width: 18px;
}
.main-title h3 {
  line-height: 22px;
  text-align: center;
  color: #000;
  font-size: 16px;
  font-weight: 400;
}
.sub-navbar {
  list-style: none;
  background: #fff;
  display: flex;
  margin-top: 43px;
  color: #000;
  padding: 10px 0;
  justify-content: center;
  align-items: center;
}
.sub-navbar li {
  font-size: 15px;
  font-weight: 300;
  padding-bottom: 5px;
  border-bottom: 3px solid transparent;
}

</style>
