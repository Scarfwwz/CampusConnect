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
    <view class="flex-item text2">密 码：</view>
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
		input2: ''
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
  background-image: url('https://ide.code.fun/api/image?token=6571d28cfcfbac0011379ca8&name=c1d62878e715f3f0304ede20ac6ddc42.png');
  background-position: 0% 0%;
  background-size: 100%, 100%;
  background-repeat: no-repeat;
  width: 750rpx;
  height: 1623.08rpx;
}
.section{
	position: absolute;
	top: 650rpx;
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
}
.text2{
	margin:8px;
}
.button1{
	position: absolute;
	top: 950rpx;
	left: 300rpx;
	width: 500rpx;
	height: 200rpx;
}
</style>