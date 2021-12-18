<template>
	<view>
		<view  class="indexBody" :style="'min-height:'+swiperHeight+'px'" >
			<view class="liuhaiclass" :style="'height:'+liuhaiHeight+'px'"></view>
			<view class="title">demo</view>
			
			
			
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				swiperHeight:0,
				liuhaiHeight:3,
				platformType:[],
			}
		},
		mounted() {
		
		},
		
		onLoad() {
			    let platform=uni.getSystemInfoSync().platform
				this.platformType.platform = platform
				this.$member.setMemberObj(this.platformType);
				this.memberData  = this.$member.memberObj
				this.liuhaiHeight = this.memberData.statusBarHeight + 10
				// this.swiperHeight  =  this.getHeight()	
				uni.getSystemInfo({
				        success:  (res) => {     // 需要使用箭头函数，swiper 高度才能设置成功
				            // 获取swiperHeight可以获取的高度，窗口高度减去导航栏高度
				            this.swiperHeight = res.windowHeight - uni.upx2px(25)
							this.liuhaiHeight = res.navigationBarHeight
				            console.log(res,2222)
				        }
				    });
		},
		
		
		onShow:function(){
		    //获取全局设置的变量
		    this.memberData = this.$member.memberObj;
			console.log(this.memberData,2225)
		
		},
		methods: {
		getData(){
						uni.getSystemInfo({
							success:  (res) => {     
								this.swiperHeight = res.windowHeight 
								console.log(this.swiperHeight)
							
							}
						});
					},
	},
	
		created() {
			this.getData()
		}
	}
</script>

<style>
</style>
