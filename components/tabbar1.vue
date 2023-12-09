<template>
	<div id="tabbar1">
		<view class="flex-row justify-center items-center relative tab-bar">
		  <view class="flex-row justify-start items-center image-wrapper pos_3" @click="back">
		    <image
		      class="image_6"
		      src="/static/icon_chevron_left.png"
		    />
		  </view>
		  <view class="flex-row justify-start items-center image-wrapper" @click="toindex">
		    <image
		      class="image_5"
		      src="/static/icon_home.png"
		    />
		  </view>
		  <view class="flex-row justify-start items-center image-wrapper pos_4" @click="toperson">
		    <image
		      class="image_6"
		      src="/static/icon_person.png"
		    />
		  </view>
		</view>
	</div>

</template>

<script>
	export default {
	name: "tabbar1",
	props: {
		type: String
	},
	components: {},
	props: {},
	data() {
	return {};
	},

	methods: {
		toindex() {
		    uni.navigateTo({
		        url: '../../pages/index/index',
		        success: res => {},
		        fail: () => {},
		        complete: () => {}
		    });
		},
		toperson() {
		    uni.navigateTo({
		        url: '../../pages/person/person',
		        success: res => {},
		        fail: () => {},
		        complete: () => {}
		    });
		},
		back() {
		    uni.navigateTo({
		        url: '../../pages/index/index',
		        success: res => {},
		        fail: () => {},
		        complete: () => {}
		    });
		},
	}
};
</script>

<style>
	.tab-bar {
	  padding: 24rpx 64rpx;
	  background-color: #d18482;
	  position: fixed; 
	  bottom: 0;
	  width: 100%;
	}
	.image-wrapper {
	  width: 80rpx;
	}
	.pos_3 {
	  position: absolute;
	  left: 63.76rpx;
	  top: 50%;
	  transform: translateY(-50%);
	}
	.image_6 {
	  width: 80rpx;
	  height: 70rpx;
	}
	.image_5 {
	  width: 80rpx;
	  height: 70rpx;
	}
	.pos_4 {
	  position: absolute;
	  right: 84rpx;
	  top: 50%;
	  transform: translateY(-50%);
	}
</style>