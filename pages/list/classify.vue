<template>
	<view>
		<view  class="indexBody" :style="'min-height:'+swiperHeight+'px'" >
			<view class="liuhaiclass" :style="'height:'+liuhaiHeight+'px'"></view>
			<view class="title">分类</view>
			<view class="classify-search">
				<view class="classify-search-content">
					<img class="classify-search-img" src="https://admin.shitutu.com/public/baiduimg/search.png" alt="">
					<input type="text" class="search-value" placeholder="搜索你喜欢的餐饮图片">
				</view>
				
			</view>
			
			<view class="classify-content-left">
				<view class="classify-one-box">
					<view class="classify-one">
						热门图片
					</view>
				</view>
				<view class="classify-one-box classify-one-box-select">
					<view class="classify-one">
						热门图片
					</view>
				</view>
				<view class="classify-one-box">
					<view class="classify-one">
						热门图片
					</view>
				</view>
				
			</view>
			
			<view class="classify-content-right">
				<view class="classify-two">
					<view class="classify-two-box">
						包子粥饼
					</view>
				</view>
				<view class="classify-two classify-two-select">
					<view class="classify-two-box">
						包子粥饼
					</view>
				</view>
				<view class="classify-two">
					<view class="classify-two-box">
						包子粥饼
					</view>
				</view>
				<view style="clear: both;"></view>
				<view class="imgListBox">
					<img src="https://image.shitutu.com/uploads/20210105/99f38c0d550522a5c10d0a50cf00107a.jpg_logo" alt="">
				</view>
			</view>
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
