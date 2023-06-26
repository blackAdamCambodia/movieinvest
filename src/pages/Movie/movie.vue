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
      <view class="index">
        <view class="movie-card">
          <view class="left-part">
            <img src="../../static/movie-banner.png" alt="" />
          </view>
          <view class="right-part">
            <view class="movie-title">
              <h4>Mission Impossible 7 : Deadly Reckoning (Part 1)</h4>
            </view>
            <view>
              <ul class="movie-rating">
                <li><img src="../../static/star.png" alt="star" /></li>
                <li><img src="../../static/star.png" alt="star" /></li>
                <li><img src="../../static/star.png" alt="star" /></li>
                <li><img src="../../static/star.png" alt="star" /></li>
                <li><img src="../../static/star.png" alt="star" /></li>
                <span class="rating">9.9</span>
              </ul>
            </view>
            <view class="movieType">
              <p>Action / Thriller / Adventure <span> IMAX 3D</span></p>
            </view>
            <view class="lunchData">
              <p>2023/07/12 North America / 156minute</p>
            </view>
            <!-- <view class="count-down">
              <span class="block">21 day</span>
              <span class="clone">:</span>
              <span class="block">12 hours</span>
              <span class="clone">:</span>
              <span class="block">34 minute</span>
              <span class="clone">:</span>
              <span class="block">36 second</span>
            </view> -->
            <view class="u-demo-block__content">
				<u-count-down
				    :time="30 * 60 * 60 * 1000"
				    format="DD:HH:mm:ss"
				    autoStart
				    millisecond
				    @change="onChange"
				>
					<view class="time count-down">
            <span class="block"><text class="time__item">{{ timeData.days }}&nbsp;day</text> </span>
              <span class="clone">:</span>
              <span class="block"><text class="time__item">{{ timeData.hours>10?timeData.hours:'0'+timeData.hours}}&nbsp;hours</text></span>
              <span class="clone">:</span>
              <span class="block"><text class="time__item">{{ timeData.minutes }}&nbsp;minute</text></span>
              <span class="clone">:</span>
              <span class="block"><text class="time__item">{{ timeData.seconds }}&nbsp;second</text></span>
						</view>
				</u-count-down>
			</view>
          </view>
        </view>
        <!-- Collapse Content start -->
        <view class="collapse-item">
          <view class="collaps-title">
            <h3>Summery</h3>
            <view class="collaps-value">
              <p class="collapsible" @click="toggleShow">
                extend
                <span class="rotate-image" @click="rotate"
                  ><img :src="imageSrc" :class="imageClasses" alt=""
                /></span>
              </p>
            </view>
          </view>
          <view v-show="collapseShow" class="collapse-content">
            <p class="summary-text" :class="{ expanded: expanded }">
              {{ getSummaryText }}
            </p>
            <view
              v-if="!expanded"
              class="show-more-btn"
              @click="expanded = true"
              >Show More</view
            >
          </view>
        </view>

        <!-- Collapse Content End -->
        <!-- cast part start -->
        <view class="main-cast">
          <view class="cast">
            <view class="cast-title">
              <h3>Cast</h3>
            </view>
            <view class="cast-people">
              <p>Total9People</p>
            </view>
          </view>
          <view class="cast-wrap">
            <view class="cast-card">
              <img src="../../static/cruise.png" alt="" />
              <h4>Cruise</h4>
              <p>Ethan Hunt</p>
            </view>
            <view class="cast-card">
              <img src="../../static/hayley.png" alt="" />
              <h4>Heyley Atwell</h4>
              <p>Grace</p>
            </view>
            <view class="cast-card">
              <img src="../../static/ving.png" alt="" />
              <h4>Ving Rhames</h4>
              <p>Luther Stickell</p>
            </view>
            <view class="cast-card">
              <img src="../../static/simon.png" alt="" />
              <h4>Simon Pegg</h4>
              <p>Benji Dunn</p>
            </view>
            <view class="cast-card">
              <img src="../../static/vanessa.png" alt="" />
              <h4>Vanessa</h4>
              <p>White Widow</p>
            </view>
            <view class="cast-card">
              <img src="../../static/rebecca.png" alt="" />
              <h4>Rebecca</h4>
              <p>llsa Faust</p>
            </view>
            <view class="cast-card">
              <img src="../../static/henry.png" alt="" />
              <h4>Henry Czerny</h4>
              <p>Eugene Kittridge</p>
            </view>
            <view class="cast-card">
              <img src="../../static/esai.png" alt="" />
              <h4>Esai Morale</h4>
              <p>Gabriel</p>
            </view>
            <view class="cast-card">
              <img src="../../static/pom.png" alt="" />
              <h4>Cruise</h4>
              <p>Ethan Hunt</p>
            </view>
          </view>
        </view>
        <!-- cast part End -->
        <!-- BlockBuster part start -->
        <view class="blockbuster">
          <view class="blockbuster-title">
            <h3>Blockbuster history</h3>
          </view>
          <view class="blockbuster-content">
            <view
              v-for="(movie, index) in movies"
              :key="index"
              class="blockbuster-card"
            >
              <span class="tag">end</span>
              <view class="movie-banner">
                <img :src="movie.bannerUrl" alt="" />
              </view>
              <view class="movie-details">
                <view class="movie-title">
                  <h4>{{ movie.title }}</h4>
                </view>
                <view class="movieType">
                  <p>Main actor：{{ movie.mainActor }}</p>
                </view>
                <view class="lunchData">
                  <p>{{ movie.releaseDate }}</p>
                </view>
                <view class="invest-details">
                  <view class="amount-of-people">
                    <p>Amount of people: {{ movie.amountOfPeople }}</p>
                  </view>
                  <view class="viewidend">
                    <p>{{ movie.dividend }}</p>
                  </view>
                </view>
              </view>
            </view>
          </view>
        </view>
        <!-- BlockBuster part End -->
      </view>
    </view>
    <view class="movie-page-footer">
      <view >
        <u-popup :round="20" :show="show" @close="close" @open="open">
          <view >
            <view class="popUp-title">
              <view class="title-left">
                <p>My level: <span>0</span>Share</p>
              </view>
              <view class="title-right">
                <h3>MGM Stock Photo</h3>
              </view>
            </view>
            <view class="popUp-content">
              <view class="assets-num">
                <view class="total-left">
                  <p>Total assets ($)</p>
                  <p>0</p>
                </view>
                <view class="total-right">
                  <p>Total assets ($)</p>
                  <p>0</p>
                </view>
              </view>
              <view >
                <ul class="popUp-card">
                  <li
                    class="popUp-card-bg"
                    v-for="item in items"
                    :key="item.shareClass"
                  >
                    <view class="two">
                      <p>{{ item.shareClass }}</p>
                      <span>{{ item.sharePercentage }}</span>
                      <p>
                        {{ item.stock
                        }}<span style="margin-left: 5px">{{
                          item.stockPrice
                        }}</span>
                      </p>
                      <span> {{ item.shareNumber }}</span>
                      <p>{{ item.shareHolder }}</p>
                    </view>
                  </li>
                </ul>
              </view>
              <view class="popUp-share">
                <span>share</span>
                <view class="form">
                  <input type="number" placeholder="Number of shares" />
                  <button type="button">Deposit($)</button>
                </view>
              </view>
            </view>
          </view>
        </u-popup>
        <button class="investmentBtn" @click="show = true">
          Join the investment
        </button>
      </view>
    </view>
  </view>
</template>
<script>
import axios from "axios";
export default {
  data() {
    return {
      title: "Movie stocks",
      show: false,
      collapseShow:false,
      movies: [],
      expanded: false,
      isRotated: false,
      timeData: {},
      items: [
        {
          shareClass: "A share",
          sharePercentage: "0.50%",
          stock: "increase stock",
          stockPrice: "100",
          shareNumber: "194320 ",
          shareHolder: "People",
        },
        {
          shareClass: "B share",
          sharePercentage: "1.00%",
          stock: "increase stock",
          stockPrice: "1000",
          shareNumber: "194450 ",
          shareHolder: "People",
        },
        {
          shareClass: "C share",
          sharePercentage: "1.50%",
          stock: "increase stock",
          stockPrice: "3000",
          shareNumber: "194237 ",
          shareHolder: "People",
        },
        {
          shareClass: "D share",
          sharePercentage: "2.00%",
          stock: "increase stock",
          stockPrice: "8000",
          shareNumber: "193580 ",
          shareHolder: "People",
        },
        {
          shareClass: "E share",
          sharePercentage: "2.10%",
          stock: "increase stock",
          stockPrice: "15000",
          shareNumber: "194568 ",
          shareHolder: "People",
        },
        {
          shareClass: "F share",
          sharePercentage: "2.20%",
          stock: "increase stock",
          stockPrice: "30000",
          shareNumber: "195656 ",
          shareHolder: "People",
        },
      ],
    };
  },
  methods: {
    open() {
      // console.log('open');
    },
    close() {
      this.show = false;
      // console.log('close');
    },
    onChange(e) {
                this.timeData = e
            },
    jumpHomePage() {
      uni.switchTab({
        url: "/pages/index/index",
      });
    },
    toggleShow() {
      this.collapseShow = !this.collapseShow;
    },
    rotate() {
      this.isRotated = !this.isRotated;
    },
  },
  onShow() {
    uni.hideTabBar();
  },
  onHide() {
    uni.showTabBar();
  },
  computed: {
    iconClass() {
      return ["iconfont", this.collapseShow ? "icon-up" : "icon-down"];
    },
    getSummaryText() {
      if (this.expanded) {
        return "Agent Ethan Hunt (Tom Cruise) and his IMF team embark on their most dangerous mission yet: Track down a new weapon that threatens the lives of all humanity, and stop it from falling into the wrong hands. At the same time, the dark forces that Ethan fought against are making a comeback, and the fate of the whole world is at stake. Facing a mysterious and powerful enemy, he had to face the ultimate choice of choosing his mission or his beloved.";
      } else {
        return "Agent Ethan Hunt (Tom Cruise) and his IMF team embark on their most dangerous mission yet...";
      }
    },
    imageSrc() {
      return this.isRotated
        ? "../../static/arrow-down.png"
        : "../../static/arrow-down.png";
    },
    imageClasses() {
      return ["image", this.isRotated ? "rotated" : ""];
    },
  },
  mounted() {
    axios
      .get("/static/json/movies.json")
      .then((response) => {
        this.movies = response.data.movies;
      })
      .catch((error) => {
        console.log(error);
      });
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
  background: url(../../static/movie-page-bg.png);
  background-repeat: no-repeat;
  background-size: 100%;
  background-color: #f5f7fa;
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
  background: rgb(229, 72, 71);
  color: #464646 !important;
  font-size: 0.37333rem;
  z-index: 99999999;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px;
}
.left-btn img {
  width: 16px;
}
.main-title h3 {
  line-height: 22px;
  text-align: center;
  color: #fff;
  font-size: 16px;
  font-weight: 400;
}
.index {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.movie-card {
  display: flex;
  justify-content: center;
  gap: 10px;
  width: 100%;
  padding: 15px 10px 10px 15px;
}
.movie-rating {
  display: flex;
  list-style: none;
  gap: 5px;
}
.rating {
  color: rgb(255, 210, 30);
  font-size: 18px;
  margin-top: -4px;
}
.left-part {
  width: 250px;
  border-radius: 8px;
}
.left-part img {
  width: 100%;
  border-radius: 8px;
}
.movie-title h4 {
  font-size: 20px;
  color: white;
  overflow: hidden;
  text-overflow: ellipsis;
  height: 30px;
  white-space: nowrap;
  width: 215px;
}
.movieType p,
.lunchData p {
  font-size: 12px;
  color: rgb(223, 223, 223);
}
.movieType span {
  background: #969799;
  color: #fff;
  font-size: 10px;
  line-height: 16px;
  border-radius: 2px;
  padding: 1px 2px;
  margin-left: 2px;
}
.count-down {
  margin-top: 20px;
}
.block {
  display: inline-block;
  width: 45px;
  color: #fff;
  font-size: 7px;
  text-align: center;
  background-color: #ee0a24;

  padding: 5px 0;
}
.clone {
  margin-left: 2px;
  color: #ee0a24;
  margin-right: 2px;
}
.rotate-image img {
  width: 14px;
  margin-left: 5px;
}
.rotated {
  transform: rotate(180deg);
}
.collapse-item {
  display: flex;
  justify-content: space-between;
  padding: 15px;
  background: #fff;
  flex-direction: column;
}
uni-view.collaps-title {
  display: flex;
  justify-content: space-between;
}
.collaps-title h3 {
  font-size: 18px;
}
.collapse-content {
  padding: 12px 0px;
  color: #969799;
  font-size: 14px;
  line-height: 1.5;
  background-color: #fff;
}
uni-view.cast {
  display: flex;
  justify-content: space-between;
  padding: 15px;
}
uni-view.cast-people p {
  color: #969799;
  text-align: right;
  font-size: 18px;
}
.cast-card {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
}
uni-view.cast-card img {
  width: 108px;
  height: 133px;
  padding: 0 12px;
}
.main-cast {
  background: #fff;
  margin-top: 15px;
}
.cast-wrap {
  display: flex;
  width: 100%;
  padding: 10px;
  overflow-x: auto;
  overflow-y: hidden;
  -webkit-overflow-scrolling: touch;
}
.cast-card h4 {
  text-align: center;
  font-size: 12px;
  padding: 5px 0;
}
.cast-card p {
  color: rgb(153, 153, 153);
  font-size: 12px;
  padding-bottom: 8px;
}
uni-view.blockbuster-title {
  background: #fff;
  margin-top: 25px;
  padding: 10px 15px;
}
.blockbuster-content {
  display: flex;
  flex-wrap: wrap;
  margin-bottom: 53px;
}
.blockbuster-card {
  width: 50%;
  border: 1px solid #ebeef5;
  background-color: #fff;
  color: #303133;
  -webkit-transition: 0.3s;
  transition: 0.3s;
  box-shadow: 0 2px 12px 0 rgba(0, 0, 0, 0.1);
  border-radius: 4px;
  overflow: hidden;
}
uni-view.movie-banner img {
  width: 100%;
  height: 100%;
  display: block;
}
uni-view.movie-details {
  padding: 10px;
}
uni-view.movie-details .movie-title h4 {
  color: #000;
  font-size: 18px;
  width: 159px;
  font-weight: 400;
  margin: 15px 0 0;
}
uni-view.movie-details .movieType p {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
  color: #000;
}
uni-view.movie-details .lunchData p {
  color: #000;
  font-size: 10px;
  margin-top: 5px;
}
uni-view.amount-of-people p {
  background-color: #ecf5ff;
  border-color: #d9ecff;
  display: inline-block;
  height: 32px;
  padding: 0 10px;
  line-height: 30px;
  font-size: 12px;
  color: #409eff;
  border-width: 1px;
  border-style: solid;
  border-radius: 4px;
  box-sizing: border-box;
  white-space: nowrap;
}
uni-view.viewidend p {
  background-color: #fef0f0;
  border-color: #fde2e2;
  color: #f56c6c;
  display: inline-block;
  height: 32px;
  padding: 0 10px;
  line-height: 30px;
  font-size: 12px;
  border-width: 1px;
  border-style: solid;
  border-radius: 4px;
  box-sizing: border-box;
  white-space: nowrap;
}
span.tag {
  position: absolute;
  z-index: 2;
  background-color: #f56c6c;
  border-color: #f56c6c;
  color: #fff;
  font-size: 12px;
  color: #fff;
  padding: 8px 10px;
  border-radius: 4px;
}

.movie-page-footer .investmentBtn {
  font-size: 18px;
  color: #fff;
  background: rgb(229, 72, 71);
  border-radius: 0px;
  z-index: 100;
  position: fixed;
  bottom: 0;
  width: 100%;
}
.collapse-content {
  max-height: 240px;
  overflow: hidden;
  transition: max-height 1s ease;
  will-change: height;
}

.expanded {
  max-height: auto !important;
}

.summary-text {
  margin: 0;
}

.show-more-btn {
  background-color: transparent;
  border: none;
  color: rgb(25, 137, 250);
  padding: 10px;
  cursor: pointer;
  font-size: 12px;
  text-align: center;
  position: relative;
}
.show-more-btn::after,
.show-more-btn::before {
  content: "";
  display: block;
  -webkit-box-flex: 1;
  -webkit-flex: 1;
  flex: 1;
  box-sizing: border-box;
  height: 1px;
  border-color: inherit;
  border-style: inherit;
  border-width: 1px 0 0;
  background: #ddd;
  top: 21px;
  position: absolute;
  width: 122px;
}
.show-more-btn::after {
  right: 0;
}
.show-more-btn::before {
  left: 0;
}
/* PopUp style start */
.popUp-title {
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #fff;
  background-image: linear-gradient(
    0deg,
    rgba(222, 112, 112, 0.53),
    rgba(255, 0, 0, 0.86)
  ) !important;
  position: relative;
  padding: 10px 16px;
  border-radius: 20px 20px 0 0;
}
.title-left span {
  color: #464646;
  font-size: 22px;
  margin: 0 5px;
}
.title-right {
  width: 50%;
}

.title-right h3 {
  font-size: 24px;
  color: #fff;
  text-align: center;
  font-weight: bold;
}
.popUp-content {
  background: #fff;
  overflow: scroll;
}
.assets-num {
  display: flex;
  justify-content: space-between;
  padding: 15px;
}
.total-left,
.total-right {
  padding: 10px;
  text-align: center;
  color: #000;
  font-size: 12px;
}
.popUp-card {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
}
.popUp-card-bg {
  background-image: url(../../static/popup-card.png);
  background-size: 100% 100%;
  margin: 0px auto;
  border-radius: 8px;
  flex-basis: 30%;
  padding: 4px;
  list-style: none;
  margin-bottom: 8px;
}
.popUp-card-bg p {
  font-size: 0.9rem;
  color: #c8c9cc;
}
.popUp-card-bg span {
  color: #ec615c;
}
.popUp-share {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px;
  position: relative;
  margin-bottom: 5px;
  padding-bottom: 24px;
}
.popUp-share > span {
  color: #646566;
  font-size: 18px;
  font-weight: bold;
}
.form {
  display: flex;
  align-items: center;
}
.form button {
  color: #fff;
  background-color: #ee0a24;
  border: 1px solid #ee0a24;
  padding: 0 15px;
  font-size: 14px;
}
.form input {
  color: #969799;
  width: 150px;
  font-size: 14px;
}
.popUp-share::after {
  position: absolute;
  box-sizing: border-box;
  content: " ";
  pointer-events: none;
  right: 16px;
  bottom: 10px;
  left: 16px;
  border-bottom: 1px solid #ebedf0;
  -webkit-transform: scaleY(0.5);
  transform: scaleY(0.5);
}

/* PopUp style End */
/* resposive style start */
@media screen and (max-width: 375px) {
  .movie-title h4 {
    font-size: 16px;
  }
  .count-down {
     margin-top: 0px;
}
  .popUp-share > span {
    font-size: 14px;
  }
  .form {
    width: 75%;
  }
  .popUp-title{
    padding: 7px 16px;
  }
  .assets-num {
    padding: 8px;
  }

  .title-right h3 {
    font-size: 21px;
  }
}
/* resposive style End */
</style>
