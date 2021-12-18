<template >
	<view>
	<view  class="indexBody" :style="'min-height:'+swiperHeight+'px'" >
		
		<view class="indexFixed" :style="{backgroundImage: 'url(' + pic_url + ')'}">
			<view class="indexHead" :style="'min-height:'+swiperHeight+'px'" >
			<view class="liuhaiclass" :style="'height:'+liuhaiHeight+'px'"></view>
				<view class="index-title" style="margin-bottom: 40rpx;">食图图</view>
				<view class="index-title" style="margin-bottom: 25rpx;">专业餐饮图库领先者</view>
				<view class="index-search">
					<img  class="index-search-img" src="https://admin.shitutu.com/public/baiduimg/search.png" alt="">
					<input type="text" class="search-value" placeholder="搜索你喜欢的餐饮图片">
				</view>
				<view class="index-content">
					<view class="fuwucontent" :style="{backgroundImage: 'url(' + bk1 + ')'}">
						<view class="fuwu-title">供需市场</view>
						<view class="fuwu-content">采购需要的餐饮 食材供应</view>
					</view>
					<view class="fuwucontent fuwucontent2" :style="{backgroundImage: 'url(' + bk2 + ')'}">
						<view class="fuwu-title">服务市场</view>
						<view class="fuwu-content">为餐饮客户提供 餐饮难题</view>
					</view>
					<view style="clear: both;"></view>
					
					<view class="index-message">
						<view class="index-message-content">今日下载:588张</view>
						<view class="index-message-content">会员开通:99人</view>
						<view class="index-message-content">更新图片:5841张</view>
					</view>
					
					<img class="index-banner" src="https://admin.shitutu.com/public/baiduimg/banner.png" alt="">
					
					<view>
						
						 <u-tabs  
						 :list="classifyList" 
						 :current="current"
						  @change="change" 
						  :bar-style="barStyle" 
						  :scrollable="false"
						  :activeStyle="barStyle" 
						  :lineColor="barStyle">
						        <view
						                slot="right"
						                style="padding-left: 4px;"
										@click="goClassify()"
						        >
						            <u-icon
						                    name="list"
						                    size="21"
						                    bold
						            ></u-icon>
						        </view>
						    </u-tabs>
							
					</view>
				</view>
				
				<view  class="more-img-box" style="column-count: 2; column-gap: 10rpx;">
				   <img  src="https://image.shitutu.com/uploads/20200715/862a8b7aae031cf28bfe6f3895cbf3c4.jpg_logo" mode="widthFix" style="break-inside: avoid; margin-bottom: 0.05rem;" />
				   <img  src="https://image.shitutu.com/uploads/20200715/3c00963d5d8511bc46311389b01be9e0.jpg_logo" mode="widthFix" style="break-inside: avoid; margin-bottom: 0.05rem;" />
				   <img  src="https://image.shitutu.com/uploads/20200715/c2cba4cca3c24b747f415d58a2443f83.jpg_logo" mode="widthFix" style="break-inside: avoid; margin-bottom: 0.05rem; " />
				   <img  src="https://image.shitutu.com/uploads/20200715/dae0c7db2d1bb6dbc6bfa88e126aab81.jpg_logo"  mode="widthFix" style="break-inside: avoid; margin-bottom: 0.05rem; " />
				   <img  src="https://image.shitutu.com/uploads/20200715/c92b3cd29a42a2ea8b2f8babf5155231.jpg_logo"  mode="widthFix" style="break-inside: avoid; margin-bottom: 0.05rem; " />
				   <img  src="https://image.shitutu.com/uploads/20200715/fc78f744433318a3d9748e2101a5cd09.jpg_logo"  mode="widthFix" style="break-inside: avoid; margin-bottom: 0.05rem; " />
				   <img  src="https://image.shitutu.com/uploads/20200715/96e4813cc602319c180cf8bcfd91b9b4.jpg_logo"  mode="widthFix" style="break-inside: avoid; margin-bottom: 0.05rem; " />
				   <img  src="https://image.shitutu.com/uploads/20200715/3658cd6a575adb32170f8bef894d8a7e.jpg_logo"  mode="widthFix" style="break-inside: avoid; margin-bottom: 0.05rem; " />
				   <img  src="https://image.shitutu.com/uploads/20200714/2c64aa11ca5b722259ec0ccfc060cf70.jpg_logo"  mode="widthFix" style="break-inside: avoid; margin-bottom: 0.05rem; " />
				   <img  src="https://image.shitutu.com/uploads/20200714/2ef0e32cfb5eabe8c9b78d147a7cb76f.jpg_logo"  mode="widthFix" style="break-inside: avoid; margin-bottom: 0.05rem; " />
				   <img  src="https://image.shitutu.com/uploads/20200714/d850c40a939dfbb145332ff0ecfd029f.jpg_logo"  mode="widthFix" style="break-inside: avoid; margin-bottom: 0.05rem; " />
				   <img  src="https://image.shitutu.com/uploads/20200713/66eb0e1b1aa6be4e4a9b4dede54be2af.jpg_logo"  mode="widthFix" style="break-inside: avoid; margin-bottom: 0.05rem; " />
				  </view>
			</view> 
			
			  
		</view>
		<view v-if="isLoginState" class="login-area" :style="'min-height:'+swiperHeight+'px'">
			
	
			<view class="card-area">
				<view class="card-area-title">请登录</view>
				<view class="card-area-introduction">登录获得更好体验</view>
				<button type="primary" class="login-btn"  open-type="getUserInfo" @getuserinfo="mpGetUserInfo">获取用户信息</button>
				<view class="card-area-introduction">暂不登录</view>
		    </view>
		</view>
	</view>
	
	</view>
</template>

<script>
	import yyVideoPlayer from '@/components/yy-video-player/yy-video-player.nvue';
	import {sendCode,classify,imgList} from '@/config/http.js';
	export default {
		data() {
			return {
				barStyle:{color:'#009DFB'},
				pic_url:'https://admin.shitutu.com/public/baiduimg/indextop.png',
				bk1:'https://admin.shitutu.com/public/baiduimg/gongxu.png',
				bk2:'https://admin.shitutu.com/public/baiduimg/fuwu.png',
				title: 'Hello',
				  current:0,
				list1: [{
				                    name: '关注',
				                }, {
				                    name: '推荐',
				                }, {
				                    name: '电影'
				                }, {
				                    name: '科技'
				                }, {
				                    name: '音乐'
				                }, {
				                    name: '美食'
				                }, {
				                    name: '文化'
				                }, {
				                    name: '财经'
				                }, {
				                    name: '手工'
				                }],
				classifyList:[],
				wagesheight: 0,
				video:'https://cdn.shitutu.com/70430.mp4',
				title: '食图图视频素材库',
				list: [],
				currentTab: 0,
				banner: [],
				navId:1,
				myData:'',
				sessionkey:'',
				openid:'',
				classify:[],
				messageContent:'',
				partner:[],
				searchType:[
					{
					    value: "1",
					    label: "视频"
					},
					{
					    value: "2",
					    label: "图片"
					},
				    {
				        value: "3",
				        label: "设计"
				    },
				        ],
				toSearchType:1,
				toSearchLabel:"视频",
				tabClick:1,
				tabHistory:2,
				historyList:[],
				searchValue:'',
				nav_content:false,
				dis_requ2:'dis_requ',
				requirements2:false,
				isLoginState:false,
				swiperHeight:0,
				userInfo:',',
				platformType:[],
				imgList:[],
				page:0,
				pagesize:6,
				cateId:82,
				loadStatus:'loading',  //加载样式：more-加载前样式，loading-加载中样式，nomore-没有数据样式
				isLoadMore:false,  //是否加载中
				noSearch:false,
				isTop :0,
				liuhaiHeight:3
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
				            console.log(this.swiperHeight)
				        }
				    });
		},
		
		
		onShow:function(){
		    //获取全局设置的变量
		    this.memberData = this.$member.memberObj;
			console.log(this.memberData,2225)
		
			// uni.getSystemInfo({
			//     success:  (res) => {     
			//         this.swiperHeight = res.windowHeight 
			// 		console.log(this.swiperHeight)
				
			//     }
			// });
		},
		methods: {
			mpGetUserInfo(result) { // 微信和百度的
				console.log('mpGetUserInfo', result);
				var that = this
				uni.login({
					  provider: 'baidu',//这里服务商名是字节跳动小程序 所以填toutiao
					  success: function (loginRes) {
						  console.log(loginRes)
						  sendCode({
						  	'code':loginRes.code,
							'iv':result.detail.iv,
							'ciphertext':result.detail.encryptedData
						  }).then(res => {
							  if(res.data.code == 1){
							    
							 that.$member.setMemberObj(res.data.data.list);
							 that.memberData  = that.$member.memberObj
							 that.openid = res.data.data.list.openid
							 that.isLoginState = true
							  console.log(that.memberData); 
							}
						   })
						},
						fail() {
							console.log(2)
						}
					});
				// ...
			},
			goClassify(){
				uni.navigateTo({
				    url: '../list/classify',
				    success: res => {},
				    fail: () => {},
				    complete: () => {}
				});
			},
		getData(){
			uni.getSystemInfo({
				success:  (res) => {     
					this.swiperHeight = res.windowHeight 
					console.log(this.swiperHeight)
				
				}
			}),
		
			classify().then(res => {
				if(res.data.code == 1){
					this.classifyList = res.data.data
					
				}else{
					 uni.showToast({title:res.data.msg,icon:'none'})
					  
				}
				
			 }),
			 imgList({
				 	'page':this.page,
				 	'pageSize':this.pagesize,
				 	'tags_id': this.cateId,
			 }).then(res => {
			 	if(res.data.code == 1){
			 		this.imgList = res.data.data.data
			 		console.log(res,88);
			 	}else{
			 		 uni.showToast({title:res.data.msg,icon:'none'})
			 		  
			 	}
			 	
			  })
		
		},
	 change(index) {
	 			if(this.current != index.index) {
	 				this.current = index.index;
	 			}
				console.log(index)
	 		},
		
	},

		created() {
			this.getData();
			
		}
	}
</script>

<style scoped lang="scss">
	.wrap {
		padding: 24rpx ;
	}

	.u-row {
		margin: 40px 0;border-radius: 10px;
	}
	
	.demo-layout {
		height: 340rpx;
		margin-bottom: 10px;
		border-radius: 5px;
		position: relative;
	}


	.displaynone{
		display: none;
	}
	.displayshow{
		display: block;
	}
	.titleNview-placing {
	        height: var(--status-bar-height);
	        padding-top: 44px;
	        box-sizing: content-box;
	    }
	
</style>
