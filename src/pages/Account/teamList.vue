<template>
  <view class="main">
    <view class="header">
      <view @click="backAccount" class="left_btn">
        <img src="../../static/back-arrow.png" alt="" />
      </view>
      <view class="Maintitle"
        ><h3>{{ title }}</h3></view
      >
      <view class="right_btn"></view>
    </view>
    <view class="time">
      <view class="date">
        <view>
          <u-datetime-picker
          :show="show"
			    v-model="value"
			    mode="date"
          cancelText="Cancle"
          confirmText="confirm"
			
          ></u-datetime-picker>
          <u-button class="datebtn"  @click="show = true">6-26-2023</u-button>
        </view>
        <span>Arrive</span>
        <view>
          <u-datetime-picker
          :show="show"
			    v-model="value"
			    mode="date"
          cancelText="Cancle"
          confirmText="confirm"           
          ></u-datetime-picker>
          <u-button class="datebtn" @click="show = true">6-26-2023</u-button>
        </view>
      </view>
      <view>
        <button class="search">search</button>
      </view>
    </view>
    <view class="count">
      <h4>Aggregated data</h4>
      <ul>
        <li>
          <h3>Team balance</h3>
          <p>$0</p>
        </li>
        <li>
          <h3>Team trading</h3>
          <p>$0</p>
        </li>
        <li>
          <h3>Total team deposit</h3>
          <p>$0</p>
        </li>
        <li>
          <h3>Total withdrawal amount</h3>
          <p>$0</p>
        </li>
        <li>
          <h3>Commission for team orders</h3>
          <p>$0</p>
        </li>
      </ul>
    </view>
    <view class="bottom"></view>
    <view class="count">
      <h4>My Team</h4>
      <ul>
        <li>
          <h3>System ID</h3>
          <h5>96149</h5>
        </li>
        <li>
          <h3>Loading for the first time</h3>
          <h5>0</h5>
        </li>
        <li>
          <h3>Team</h3>
          <h5>0</h5>
        </li>
        <li>
          <h3>Level 1</h3>
          <h5>0</h5>
        </li>
        <li>
          <h3>New registration</h3>
          <h5>0</h5>
        </li>
        <li>
          <h3>Active activities</h3>
          <p>0</p>
        </li>
      </ul>
    </view>
    <view class="nav">
      <u-subsection :list="list"
					mode="button"
					:current="current"
					activeColor="#007aff"
          bgColor="#e7f3fd"
					@change="change">
        </u-subsection>
    </view>
    <view>
      <p class="no-more">No figures available</p>
    </view>
    
    <custom-tab-bar direction="horizontal" class="team-footer" />
  </view>
</template>

<script>
export default {
  data() {
    
    return {
      title: "Team",
      show: false,	
      list: ['Level 1', 'Level 2','Level 3'],
			current: 0	,
      value: Number(new Date()),
				
      };
  },
  
  methods: {
    backAccount() {
      uni.navigateBack({
        url: "/pages/Account/myaccount",
      });
    },
    change(index) {
				this.current = index
			},
  },
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
  background: #e54847;
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
.Maintitle h3 {
  color: #f2f2f2;
  font-size: 17px;
  font-weight: 400;
}
uni-view.time {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 40px 10px 14px;
}
.time p {
  background: #fff;
  border: 2px solid #cdcdcd;
  padding: 8px 10px;
  font-size: 12px;
  border-radius: 40px;
}
uni-view.date {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.date span {
  font-size: 14px;
  margin-left: 8px;
  margin-right: 8px;
}
button.search {
  background: #ff7614 url(../../static/search-icon.png) no-repeat 12px;
  background-size: 20px;
  border-radius: 40px;
  padding: 10px 16px 10px 32px;
  line-height: 20px;
  float: right;
  color: #fff;
  font-size: 14px;
}
.count {
  background: #fff;
  border-radius: 10px;
  padding: 0 15px 15px;
  margin-bottom: 10px;
}
.count h4 {
  font-size: 18px;
  line-height: 50px;
  border-bottom: 1px solid #e8e8e8;
  font-weight: 700;
}
.count ul {
  display: flex;
  flex-wrap: wrap;
}
.count ul li {
  list-style: none;
  width: 33.33%;
  padding: 10px 0;
  text-align: center;
  border-right: 1px dotted #eee;
}
.count ul li:nth-child(3n + 0) {
  border-right: none !important;
}
.count ul li h3 {
  font-size: 14px;
  color: #979797;
  font-weight: 400;
}
.count ul li p {
  color: #ff6c02;
  font-size: 18px;
  margin-top: 10px;
}
.count ul li h5 {
  font-weight: 400;
  font-size: 20px;
  margin-top: 10px;
}
.nav {
  display: flex;
  align-items: center;
  margin: 15px auto 0;
  background: #f2f2f2;
  padding-top: 15px;
}

.__avatar {
			background-color: #fff;
			padding: 5px;
			border-radius: 3px;
      border: 1px solid #cdcdcd;
		}
.u-subsection--button {
    padding: 0px;
    border: 1px solid skyblue;
    border-left: 0;
    border-right: 0;
}
.no-more {
  text-align: center;
  font-size: 12px;
  padding: 20px 0;
  color: #979797;
  background: #f2f2f2;
}
.team-footer {
  position: fixed;
  bottom: 0;
  padding: 10px 0px !important;
  box-shadow: 10px 0px 10px #ddd !important;
  background: #fff;
}
.bottom {
  background: #f2f2f2;
  height: 10px;
}
/* date popUp style start */
.datebtn {
  border:2px solid #979797;
  border-radius: 20px ;
}
/* date popUp style end */
/* resposive style start */
@media screen and (max-width: 375px) {
  .datebtn {
  font-size: 12px;
  padding: 0 5px;
  height: 30px;
}
button.search {
  background-size: 13px;
  padding: 8px 9px 8px 26px;
  line-height: 14px;
  font-size: 12px;
  }
  .no-more{
    margin-bottom: 57px;
  }
}
/* resposive style End */
</style>
