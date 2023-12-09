<template>
	<view>
		<el-col :span="2">
			<el-menu class="mymenu">
			  <el-menu-item index="1">
				<i class="el-icon-user"></i>
			  </el-menu-item>
			  <el-menu-item index="2">
				<i class="el-icon-thumb"></i>
			  </el-menu-item>
			  <el-menu-item index="3">
				<i class="el-icon-location-information"></i>
			  </el-menu-item>
			  <el-menu-item index="4">
				<i class="el-icon-chat-round"></i>
			  </el-menu-item>
			</el-menu>
		</el-col>
		

	</view>

</template>

<script>
	export default {
	data() {
	  return {
		tabPosition: 'left'
	  };
	}
	};
</script>

<style>
	.mymenu{
		width:130rpx;
	}
</style>