<template>
<div class="page">
<view class="uni-flex uni-column section">
  <view class="uni-flex uni-row section1">
    <view class="flex-item text1">用户名：</view>
    <view class="flex-item input1">
      <el-input placeholder="请输入内容" v-model="input1"></el-input>
    </view>
  </view>
  <view class="uni-flex uni-row section1">
    <view class="flex-item text2"> {{password}}</view>
    <view class="flex-item input2">
      <el-input placeholder="请输入内容" v-model="input2"></el-input>
    </view>
  </view>
</view>
<view class="button1">
	<el-button type="primary" plain @click="toIndex">登录</el-button>
</view>
</div>
</template>

<script>
export default {
  components: {},
  props: {},
  data() {
    return {
		input1: '',
		input2: '',
		password:"密 码 ："
	};
  },

  methods: {
	  toIndex() {
		uni.navigateTo({
			url: '../index/index',
			success: res => {},
			fail: () => {},
			complete: () => {}
		  });
		}
  }
};
</script>

<style scoped lang="css">
.page {
  background-image: url('https://ide.code.fun/api/image?token=65725d0dfcfbac001137a3e1&name=4a7f8af900053e9ef5eb1ae3aaf3fd63.png');
  background-position: 0% 0%;
  background-size: 100%, 100%;
  background-repeat: no-repeat;
  width: 750rpx;
  height: 1623.08rpx;
}
.section{
	position: absolute;
	top: 600rpx;
	left: 50rpx;
	width: 500rpx;
	height: 200rpx;
	border: 0;
}
.section1{
	display: flex; /* 使用 Flexbox 布局 */
	justify-content: space-between; /* 水平分布，两侧对齐 */
	margin:20px;
}
.text1{
	margin:3px;
	color: white;
	font-weight:400;
	font-size: 120%;
}
.text2{
	margin:8px;
	color: white;
	font-weight:400;
	font-size: 120%;
}
.button1{
	position: absolute;
	top: 950rpx;
	left: 300rpx;
	width: 500rpx;
	height: 200rpx;
}
</style>