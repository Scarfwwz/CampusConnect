<template>
	<view class="flex-col page">
	  <view class="flex-col flex-1 group">
	    <view class="flex-col">
	      <image
	        class="image"
	        src="https://ide.code.fun/api/image?token=6571d28cfcfbac0011379ca8&name=14fdb80c70fdf6b4accc31ba91d8577c.png"
	      />
	      <view class="flex-row justify-center items-center relative section">
	        <image
	          class="image_2"
	          src="https://ide.code.fun/api/image?token=6571d28cfcfbac0011379ca8&name=4063dafd45eacfb84bb892e569c8e19c.png"
	        />
	        <text class="ml-10 font text">招聘信息发布</text>
	      </view>
	      <view class="flex-col justify-start relative group_2">
	        <view class="relative section_2"></view>
	        <image
	          class="image_3 pos"
	          src="https://ide.code.fun/api/image?token=6571d28cfcfbac0011379ca8&name=4679664c74e96dc3f8e657d9aef2a545.png"
	        />
	        <text class="font pos_2">校企交流预约</text>
	      </view>
	    </view>
	    <view class="mt-30 flex-row justify-center items-center section_3">
	      <image
	        class="image_4"
	        src="https://ide.code.fun/api/image?token=6571d28cfcfbac0011379ca8&name=e2a66e644ff7d17a05df83659ad7928c.png"
	      />
	      <text class="ml-8 font text_2">就业需求查询</text>
	    </view>
	  </view>

	  <tabbar1></tabbar1>

	</view>
</template>

<script>
	import tabbar1 from '../../components/tabbar1.vue'
	export default {
	  components: {
		  tabbar1
	  },
	  props: {},
	  data() {
	    return {};
	  },
	
	  methods: {},
	};
</script>

<style>
.page {
  background-image: linear-gradient(180deg, #efcdcf 0%, #efcdcf00 100%);
  width: 100%;
  overflow-y: auto;
  overflow-x: hidden;
  height: 100%;
}
.group {
  padding: 144rpx 84rpx 132rpx;
  overflow-y: auto;
}
.image {
  margin: 0 16rpx;
  width: 548rpx;
  height: 302rpx;
}
.section {
  margin-top: 18rpx;
  padding-bottom: 8rpx;
  background-color: #f4b4bb;
  border-radius: 48rpx;
  box-shadow: 0rpx 8rpx 8rpx #00000040;
}
.image_2 {
  border-radius: 28rpx;
  width: 152rpx;
  height: 158rpx;
}
.group_2 {
  padding-top: 60rpx;
}
.section_2 {
  background-color: #a19cf2c9;
  border-radius: 48rpx;
  box-shadow: 0rpx 8rpx 8rpx #00000040;
  height: 168rpx;
}
.image_3 {
  width: 190rpx;
  height: 190rpx;
}
.pos {
  position: absolute;
  left: 33rpx;
  bottom: 0;
}
.section_3 {
  background-color: #f4b4ba;
  border-radius: 48rpx;
  box-shadow: 0rpx 8rpx 8rpx #00000040;
}
.image_4 {
  width: 170rpx;
  height: 176rpx;
}
.font {
  font-size: 48rpx;
  font-family: Kumbh Sans;
  line-height: 44.44rpx;
  color: #ffffff;
}
.pos_2 {
  position: absolute;
  right: 72.46rpx;
  bottom: 63.96rpx;
}
.text {
  line-height: 44.78rpx;
}
.text_2 {
  line-height: 44.26rpx;
}
.tab-bar {
  padding: 24rpx 64rpx;
  background-color: #d18482;
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
  width: 54rpx;
  height: 54rpx;
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