<template>
  <view class="content">
      <view class="topRight">
        <image class="countryFlag" src="/static/us-flag.png"></image>
        <text class="language">{{ language }}</text>
      </view>
      <view class="logo">
        <img class="mgm-logo"  src="/static/mgm-logo.png" alt="">
        <text class="title">{{ title }}</text>
      </view>
    
    <!-- login -->
    <view class="form" v-if="isLogin">
      <view class="uni-form-item uni-column">
        <image class="contact" src="/static/contact-icon.png"></image>
        <input
          class="uni-input"
          type="tel"
          placeholder="Phone"
          required
          v-model="phone"
        />
      </view>
      <view class="uni-form-item uni-column">
        <image class="lock" src="/static/lock.png"></image>
          <input
            class="uni-input"
            placeholder="Enter Password"
            :password="showPassword"
            v-model="showPassword"
            required
            type="password"
          />
      
      </view>      
       <view class="option">
        <view class="auto"> 
          <checkbox class="autoLogin" value="cb" checked="false" style="transform: scale(0.7)" /> 
          <span>Automatic login </span>
        </view>
        <view>
          <p class="customerService" @click="jumpService">Online Customer Service</p>
        </view>
       </view>   
      <input
        type="submit"
        @click="jumpHomePage"
        class="loginbtn"
        value="Log in"
      />
      <view class="signUpbtn" v-if="isLogin">
        <p>Do not have an account? 
          <span @click="goRegister" class=""> Sign up now</span>
        </p>
    </view>
      <view class="download">
        <h3 class="downloadApp">Download the App</h3>
        <p>Ver.&nbsp;1.29</p>
      </view>
    </view>
    <!-- register -->
    <view class="form" v-if="!isLogin">
      <view class="uni-form-item uni-column">
        <image class="contact" src="/static/contact-icon.png"></image>
        <input class="uni-input" type="tel" v-model="phone" placeholder="Phone" />
      </view>
      <view class="uni-form-item uni-column">
        <image class="lock" src="/static/lock.png"></image>
        <view class="input-wrapper">
          <input
          type="password"
            class="uni-input"
            placeholder="Enter Password"
            :password="showPassword"
            v-model="password"
          />
          <view
            class="uni-icon"
            :class="[!showPassword ? 'uni-eye-active' : '']"
            @click="changePassword"
          >
            <image
              class="closeEye"
              @click="value > 0 ? value-- : value++"
              :src="passwordShow"
            ></image>
          </view>
        </view>
      </view>
      <view class="uni-form-item uni-column">
        <image class="lock" src="/static/lock.png"></image>
        <view class="input-wrapper">
          <input
          type="password"
            class="uni-input"
            placeholder="Confrim Password"
            :password="showPassword"
            v-model="confirmPassword"
          />
          <text
            class="uni-icon"
            :class="[!showPassword ? 'uni-eye-active' : '']"
            @click="changePassword"
          >
            <image
              class="closeEye"
              @click="otherValue > 1 ? otherValue-- : otherValue++"
              :src="confrimPassword"
            ></image>
          </text>
        </view>
      </view>
      <view class="uni-form-item uni-column">
        <image class="inboxmsg" src="/static/inbox-msg.png"></image>
        <input class="uni-input" type="number" placeholder="Referral code" v-model="referralCode" />
      </view>
      <view class="uni-form-item uni-column">
        <image class="inboxmsg" src="/static/inbox-msg.png"></image>
        <input
          class="uni-input"
          type="text"
          placeholder="Please enter a nickname"
          v-model="nickname"
        />
      </view>
      <view class="uni-form-item uni-column">
        <image class="inboxmsg" src="/static/inbox-msg.png"></image>
        <input
          class="uni-input"
          type="date"
          placeholder="Please select your data of birth"
        />
      </view>
      <button type="warn" class="registerBtn">Register</button>
      <view class="signUpbtn" v-if="!isLogin">
        <p>Have account? <span @click="goLogin">Now login</span></p>
        
      </view>
    </view>   
    
    
  </view>
</template>
<script>

export default {
  data() {
    return {
      title:"MGM",
      language:'English',     
      isLogin: true,
      value:0,
      otherValue:1,
      phone: '',
      password: '',
      confirmPassword: '',
      referralCode: '',
      nickname: '',
      showPassword: false,
      
    };
    
  },
  
  methods: {
    goLogin() {
      this.isLogin = true;
    },
    goRegister() {
      this.isLogin = false;
    },
    jumpService() {
      uni.switchTab({
        url: "/pages/customer/customerService",
      });
    },
    jumpHomePage() {
      uni.switchTab({
        url: "/pages/index/index",
      });
    },
  },
  computed: {
    passwordShow(){
        return this.value == 0 ? '/static/close-eye.png' : '/static/open-eye.png'
    },
    confrimPassword(){
        return this.otherValue == 1 ? '/static/close-eye.png' : '/static/open-eye.png'
    }
   
  }
};
</script>

<style>
.content {
  background: url(../../static/banner.png) no-repeat;
  background-size: 100%;
  /* padding: 45px 32px 0px;
  min-height: 100vh;
  margin-top: -45px; */
  display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    padding: 30px;
}
.logo {
  padding-top: 145px;
}
.mgm-logo {
  width: 80px;
  margin: 0 auto;
  display: block;
  border-radius: 50%;
  animation: rotateImage 10s linear infinite;
}
@keyframes rotateImage {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
.form {
    margin-top: 40px;
}
.title {
  font-size: 27px;
  color: rgb(205, 92, 92);
  display: flex;
  justify-content: center;
  font-weight: 500;
}
.topRight {
  position: absolute;
  right: 0.26667rem;
  top: 50px;
  display: flex;
  align-items: center;
  background: rgba(255, 255, 255, 0.2);
  border-radius: 30px;
  padding: 8px 10px;
}
.countryFlag {
  width: 1.5rem;
  height: 1rem;
}
.language {
  margin-left: 5px;
  color: #fff;
  font-size: 12px;
}
.download {
    margin-top: 40px;
}
.contact,
.lock,
.inboxmsg,
.closeEye {
  width: 1.4rem;
  height: 1.2rem;
}
.uni-form-item {
  display: flex;
  border-bottom: 1px solid #f1f1f1;
  height: 50px;
  align-items: center;
}
.uni-input {
  width: 100%;
  margin-left: 15px;
}
.input-wrapper {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 270px;
}
.auto {
  display: flex;
  align-items: center;
}
.loginbtn {
  border-radius: 40px;
  background: rgb(229, 72, 71);
  color: #fff;
  font-size: 20px;
  margin: 35px auto;
  padding: 10px 15px;
  text-align: center;
}
.registerBtn {
  border-radius: 40px;
  background: rgb(229, 72, 71);
  color: #fff;
  font-size: 20px;
  margin: 35px auto;
  padding: 0px 15px;
  text-align: center;
}
.signUpbtn  {
  color: #696969;
  text-align: center;
  font-size: 15px;
 
}

.option {
  display: flex;
  color: #696969;
  font-size: 16px;
  justify-content: space-between;
  list-style: none;
  margin: 20px auto;
}
.signUpbtn p span {
  color:red;
  margin-left: 7px;
}

.download h3 {
  width: 100px;
  line-height: 30px;
  padding: 4px;
  font-size: 16px;
  font-weight: 400;
  color: #000;
  border: 1px solid #555;
  border-radius: 20px;
  margin: 0 auto;
  text-align: center;
}
.download p {
  color: #000;
  text-align: center;
  display: block;
  margin: 10px 0;
  font-size: 12px;
  
}
@media screen and (max-width: 414px) {
  .logo {
    padding-top: 170px;
  }
}
@media screen and (max-width: 375px) {
  .logo {
    padding-top: 150px;
  }
}
@media screen and (max-width: 340px) {
  .logo {
    padding-top: 125px;
  }
  .signUpbtn {
    font-size: 12px;
  }
}
</style>
