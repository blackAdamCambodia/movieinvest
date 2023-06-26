<template>
  <view class="main">
    <view class="header">
      <view class="left_btn">
        <img @click="backAccount" src="../../static/back-arrow.png" alt="" />
      </view>
      <view class="Maintitle"
        ><h3>{{ title }}</h3></view
      >
      <view class="right_btn">
        <h3>History</h3>
      </view>
    </view>
    <view class="price">
      <a href=""><span>+</span>Wallet address</a>
    </view>
    <view class="count">
      <input type="text" placeholder="Enter the amount you want to withdraw" />
    </view>
    <view class="select-option">
      <ul>
        
          <radio-group @change="radioChange">
				<li class="uni-list" v-for="(item, index) in items" :key="item.value">
          <view class="erc20">
            <img :src="item.icon" alt="" />
            <h4>{{ item.label }}</h4>
          </view>
					<view>
						<radio :value="item.value"  style="transform: scale(0.7)"  color="#FFCC33" :checked="index === current" />
					</view>        
          
				</li>
			</radio-group>
        
      </ul>
    </view>
    <view class="txsmf"></view>
    <button type="button">Withdraw money now</button>
  </view>
</template>

<script>
export default {
  data() {
    return {
      title: "Withdrawal management",
      items: [
                {
                  label: "USDT-ERC20",
                  value: "USDT-ERC20",
                  name:'checkUsdt',
                  icon: "../../static/trc-icon.png",
                  checked: 'true'
                },
                {
          label: "USDT-TRC20",
          value: "USDT-TRC21",
          name:'checkUsdt',
          icon: "../../static/trc-icon.png",
        },
        { label: "Visa",
        name:'checkUsdt',
         value: "Visa", 
         icon: "../../static/visa-card.jpeg" 
        }
            ],
            current: 0
    }
   
  },
  methods: {
    backAccount() {
      uni.navigateBack({
        url: "/pages/Account/myaccount",
      });
    },
    radioChange: function(evt) {
            for (let i = 0; i < this.items.length; i++) {
                if (this.items[i].value === evt.detail.value) {
                    this.current = i;
                    break;
                }
            }
        }
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
  padding: 10px;
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
  padding: 14px 10px;
}
.left_btn img {
  width: 15px;
  height: 15px;
}
.Maintitle h3 {
  font-size: 16px;
  font-weight: 400;
}
.right_btn h3 {
  font-size: 10px;
}
.price {
  background: url(../../static/cash-bg.png) no-repeat;
  background-size: 100%;
  height: 125px;
  border-radius: 10px;
  position: relative;
  margin: 30px 10px 0px;
}
.price a {
  position: absolute;
  top: 20px;
  z-index: 9;
  left: 25px;
  text-decoration: none;
  color: #fff;
  width: 100%;
  display: block;
  font-size: 14px;
}
.price span {
  color: #ea4f76;
  border: 1px solid #fff;
  width: 24px;
  height: 24px;
  border-radius: 50%;
  margin-right: 10px;
  text-align: center;
  line-height: 22px;
  display: inline-block;
}
.count input,
.txsmf {
  color: #9b9ba4;
  background-color: #f1f1f1;
  margin: 15px;
  padding: 15px 12px;
  height: 50px;
  border-radius: 6px;
}
.select-option {
  padding: 0 22px;
}
.uni-list {
  display: flex;
  justify-content: space-between;
  
}
.select-option ul {
  border-bottom: 1px solid #dddee1;
}
.select-option ul li {
  display: flex;
  justify-content: space-between;
  padding: 5px 0;
  list-style: none;
}
.select-option ul li img {
  width: 20px;
  height: 20px;
}
.erc20 {
  display: flex;
  justify-content: space-between;
  gap: 10px;
}
.erc20 h4 {
  font-weight: 400;
  font-size: 14px;
}
.txsmf {
  padding: 5px !important;
  height: 36px;
}
button {
  color: #fff;
  text-align: center;
  border-radius: 8px;
  background-image: linear-gradient(0deg, #fc4f00, #fd9000);
  margin: 12px;
  font-size: 20px;
}
</style>
