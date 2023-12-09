<template>
	<view class="flex-col page">
	  <view class="flex-col justify-start items-center flex-1 group">
		<view class="flex-col relative section">
			<image class="image pos"src="https://ide.code.fun/api/image?token=6573dbf828456c00116909af&name=4063dafd45eacfb84bb892e569c8e19c.png"/>
			<text class="self-end text">招聘信息发布</text>
		  <el-form ref="form" :model="form"  label-width="150rpx" label-position="left">
			 <el-form-item label="企业名称">
		      <el-input v-model="form.firmName"></el-input>
		    </el-form-item>
		    <el-form-item label="企业简介">
		      <el-input type="textarea" v-model="form.introduction"></el-input>
		    </el-form-item>
			<el-form-item label="招聘岗位">
			  <el-input v-model="form.position"></el-input>
			</el-form-item>
			<el-form-item label="薪资待遇">
			  <el-input v-model="form.salary"></el-input>
			</el-form-item>
			<el-form-item label="就业城市">
			  <el-input v-model="form.city"></el-input>
			</el-form-item>
			<el-form-item label="招聘链接">
			  <el-input v-model="form.link"></el-input>
			</el-form-item>
		    <el-form-item label="宣讲时间">
		      <el-col :span="11">
		        <el-date-picker type="date"  v-model="form.date1" style="width: 100%;"></el-date-picker>
		      </el-col>
		      <el-col class="line" :span="2">-</el-col>
		      <el-col :span="11">
		        <el-time-picker  v-model="form.date2" style="width: 100%;"></el-time-picker>
		      </el-col>
		    </el-form-item>
			<el-form-item label="宣讲地点">
			  <el-input v-model="form.location"></el-input>
			</el-form-item>
			<el-form-item label="其他信息">
			  <el-input type="textarea" v-model="form.otherInfo"></el-input>
			</el-form-item>
			
		  </el-form>		  
	    </view>
		<view class="flex-col justify-start items-center button text-wrapper" @click="onSubmit">
			<text class="text_2">提交</text>
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
      return {
        form: {
          firmName: '',
          introduction: '',
		  position:'',
		  salary:'',
		  city:'',
		  link:'',
          date1: '',
          date2: '',
          location:'',
		  otherInfo:''
        }
      }
    },
    methods: {
      onSubmit() {
        this.$confirm('是否确认发布信息', '确认', {
                  confirmButtonText: '确定',
                  cancelButtonText: '取消',
                  type: 'warning',
				  class:'mybox'
                }).then(() => {
                  this.$message({
                    type: 'success',
                    message: '发布成功!'
                  });
                }).catch(() => {
                  this.$message({
                    type: 'info',
                    message: '已取消'
                  });          
                });
      }
    }
};
</script>

<style>
.page {
  background-image: linear-gradient(180deg, #efcdcf 0%, #efcdcf00 100%);
  width: 100%;
  overflow-y: auto;
  overflow-x: hidden;
}

.group {
  padding: 100rpx 0 54rpx;
  overflow-y: auto;
}
.section {
  padding: 160rpx 15rpx 15rpx 15rpx;
  background-color: #f4b4bb;
  border-radius: 48rpx;
  box-shadow: 0rpx 8rpx 8rpx #00000040;
  width: 580rpx;
  height:750rpx;
}
.myform{
	height: 375px; /* 设置容器的高度，超出这个高度将出现滚动条 */
	overflow-y: scroll; /* 显示垂直滚动条 */
}
.text {
  color: #ffffff;
  font-size: 48rpx;
  font-family: Kumbh Sans;
  line-height: 44.78rpx;
  position: absolute;
  left: 250rpx;
  top: 60rpx;  
}
.button {
  align-self: flex-start;
  margin-top: 70rpx;
}
.text-wrapper {
  padding: 56rpx 0;
  background-color: #d18482;
  border-radius: 40rpx;
  width: 306rpx;
  position: absolute;
  bottom:170rpx;
  left:230rpx;
}
.text_2 {
  color: #ffffff;
  font-size: 40rpx;
  font-family: Kumbh Sans;
  line-height: 37rpx;
}
.image {
  border-radius: 28rpx;
  width: 152rpx;
  height: 158rpx;
}
.pos {
  position: absolute;
  left: 44.68rpx;
  top: 0;
}

</style>