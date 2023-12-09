<template>
	<view class="flex-col page">
	  <view class="flex-col justify-start items-center flex-1 group">
		<view class="flex-col relative section">
			<image class="image pos"  src="https://ide.code.fun/api/image?token=6573dbf828456c00116909af&name=3d5533c9b933ad3a949b251d2d29bbaa.png"/>
			<text class="self-end text">校企交流预约</text>
		  <el-form ref="form" :model="form" class="myform" label-width="150rpx" label-position="left">
			 <el-form-item label="企业名称">
		      <el-input v-model="form.firmName"></el-input>
		    </el-form-item>
			<el-form-item label="您的姓名">
			  <el-input v-model="form.yourName"></el-input>
			</el-form-item>
			<el-form-item label="来访人数">
			  <el-input v-model="form.personNumber"></el-input>
			</el-form-item>
			<el-form-item label="联系电话">
			  <el-input v-model="form.telephone"></el-input>
			</el-form-item>
			<el-form-item label="来访时间">
			  <el-col :span="11">
			    <el-date-picker type="date"  v-model="form.date1" style="width: 100%;"></el-date-picker>
			  </el-col>
			  <el-col class="line" :span="2">-</el-col>
			  <el-col :span="11">
			    <el-time-picker  v-model="form.date2" style="width: 100%;"></el-time-picker>
			  </el-col>
			</el-form-item>
			<el-form-item label="备注">
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
          yourName: '',
		  personNumber:'',
		  telephone:'',
          date1: '',
          date2: '',
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