<template>
	<div>
		<view class="l-top">
		    <view class="l-red">
		        <button  class="l-red" >
		            <image class="user-pic" src="../../static/hr.png"></image>
		            <view class="user-name">金山软件招聘经理</view>
		        </button>
		    </view>
		</view>
		<view class="c-row">
		    <view class="c-bottom">
		        <view  class="c-cxsc">
		            <image class="cxsc-img" src="/static/icon_home.png"></image>
		            <view class="cxsc-txt">
		                <view>车型收藏</view>
		                <view class="txt-gray">意向车型</view>
		            </view>
		        </view>
		        <view  class="c-pybxc">
		            <image class="bxc-img" src="/static/icon_person.png"></image>
		            <view class="bxc-txt">
		                <view>朋友帮选车</view>
		                <view class="txt-gray">发起投票</view>
		            </view>
		        </view>
		    </view>
		</view>
		<view class="f">
		    <view  class="f-row">
		        <image class="f-img" src="/static/icon_person.png"></image>
		        <view class="f-txt">询价记录</view>
		        <view class="f-right tip-right"></view>
		    </view>
		    <view  class="f-row">
		        <image class="f-img" src="/static/icon_person.png"></image>
		        <view class="f-txt">意见反馈</view>
		        <view class="f-right tip-right"></view>
		    </view>
		    <view  class="f-row">
		        <image class="f-img" src="/static/icon_person.png"></image>
		        <view class="f-txt">关于我们</view>
		        <view class="f-right tip-right"></view>
		    </view>
		</view>
		<view class="b">
		    <Text >退出登录</Text>
		</view>
		
	</div>

</template>

<script>
</script>

<style>
	.l-red {
	    margin: 0;
	    padding-top: 10px;
	    background:  #d18482;
	    text-align: center;
	}
	
	.l-blue::after {
	    border: none;
	}
	
	.user-pic {
	    border-radius: 50%;
	    border: solid 5px #f4b4bb;
	    box-shadow: 0 0 0 5px #efcdcf;
		background-repeat: no-repeat;
		width: 150rpx;
		height: 150rpx;
	}
	
	.user-name {
	    width: 360rpx;
	    margin-top: 20rpx;
	    font-size: 36rpx;
	    color: #fff;
	    margin: 0 auto;
	    overflow: hidden;
	    text-overflow: ellipsis;
	    white-space: nowrap;
	}
	
	.bk-bottom {
	    display: block;
	    width: 100%;
	    height: 40rpx;
	}
	
	.c-row {
	    height: 180rpx;
	    box-sizing: border-box;
	    padding: 0 0 0 30rpx;
	}
	
	.c-bottom {
	    border-bottom: solid 1px #f5f5f5;
	}
	
	.c-cxsc,.c-pybxc {
	    width: 50%;
	    display: inline-block;
	    text-align: left;
	    vertical-align: middle;
	}
	
	.c-cxsc .cxsc-img {
	    width: 80rpx;
	    height: 80rpx;
	}
	
	.c-cxsc .cxsc-txt,.c-pybxc .bxc-txt {
	    display: inline-block;
	    margin: 44rpx 30rpx;
	    font-size: 32rpx;
	    color: #333;
	}
	
	.txt-gray {
	    font-size: 24rpx;
	    color: #999;
	    margin-top: 10rpx;
	}
	
	.c-pybxc .bxc-img {
	    width: 80rpx;
	    height: 80rpx;
	}
	
	.f {
	    padding: 0 0 0 30rpx;
	}
	
	.f .f-row {
	    display: flex;
	    align-items: center;
	    border-bottom: solid 1px #f5f5f5;
	    padding: 34rpx 30rpx 34rpx 0;
	}
	
	.f-img {
	    width: 32rpx;
	    height: 32rpx;
	}
	
	.f-txt {
	    flex: 1;
	    font-size: 32rpx;
	    color: #666;
	}
	
	.f-txt {
	    margin-left: 30rpx;
	}
	
	.b {
	    position: fixed;
	    width: 100%;
	    bottom: 0;
	    text-align: center;
	    padding: 0 0 0 30rpx;
	    box-sizing: border-box;
	    font-size: 34rpx;
	    height: 100rpx;
	    line-height: 100rpx;
	    color: #5f93ff;
	}
</style>