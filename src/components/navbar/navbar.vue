<template>
	<view>
		<u-tabbar
			:value="tabbarChange"
			:border="false"
			:fixed="true"
			:placeholder="true"
			:safeAreaInsetBottom="true"
		>
			<u-tabbar-item text="Home" @click="UpdateTabbarChange">
				<image class="u-page__item__slot-icon" slot="active-icon" src="@/static/home-icon.png"></image>
				<image class="u-page__item__slot-icon" slot="inactive-icon" src="@/static/redhome-icon.png"></image>
			</u-tabbar-item>
			<u-tabbar-item text="History" @click="UpdateTabbarChange">
				<image class="u-page__item__slot-icon" slot="active-icon" src="@/static/history-icon.png"></image>
				<image class="u-page__item__slot-icon" slot="inactive-icon" src="@/static/redhistory-icon.png"></image>
			</u-tabbar-item>

			<u-tabbar-item text="movie" class="center-button" @click="UpdateTabbarChange" >
				<image class="u-page__item__slot-icon" slot="active-icon" src="@/static/movie-icon.png"></image>
				<image class="u-page__item__slot-icon" slot="inactive-icon" src="@/static/redmovie-icon.png"></image>
			</u-tabbar-item>

			<u-tabbar-item text="Customer" @click="UpdateTabbarChange">
				<image class="u-page__item__slot-icon" slot="active-icon" src="@/static/customer-icon.png"></image>
				<image class="u-page__item__slot-icon" slot="inactive-icon" src="@/static/redcustomer-icon.png"></image>
			</u-tabbar-item>
			<u-tabbar-item text="account" @click="UpdateTabbarChange">
				<image class="u-page__item__slot-icon" slot="active-icon" src="@/static/footer-contact-icon.png"></image>
				<image class="u-page__item__slot-icon" slot="inactive-icon" src="@/static/redcontact-icon.png"></image>
			</u-tabbar-item>
		</u-tabbar>
	</view>
</template>
<script>

import {mapState} from "vuex";
export default {
	data() {
		return {
			list: [
				'/pages/index/index',
				'/pages/History/history',
				'/pages/Movie/movie',
				'/pages/customer/customerService',
				'/pages/Account/myaccount',
				

			],
		};
	},
	computed: {
		...mapState([
			'tabbarChange',
		]),
	},
	watch: {

	},
	methods: {
		UpdateTabbarChange(index){
			console.log(index)
			uni.$u.route({url:this.list[index],type:'redirect'});
			store.dispatch('UpdateTabbarChange', index);
		}
	},

	mounted() {
	},
	
	destroyed() {
	},
};
</script>
<style>

	.u-page__item__slot-icon{
		width: 20px;
		height: 20px;
	}
	.u-tabbar {
	position: fixed;
    left: 0;
    bottom: 0;
    width: 100%;
    background: url(../../static/footer-bg.png) no-repeat bottom;
    background-size: 100%;
    z-index: 999;
    height: 1.73333rem;
	}
</style>
