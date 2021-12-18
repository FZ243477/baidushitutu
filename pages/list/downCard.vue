<template>
	<view>
		<view  class="indexBody balck-down" :style="'min-height:'+swiperHeight+'px'" >
			<view class="liuhaiclass" :style="'height:'+liuhaiHeight+'px'"></view>
			<view class="title" style="color: #FFFFFF;">下载卡</view>
			
			<view class="down-user" :style="{backgroundImage: 'url(' + pic_url + ')'}">
				<view  class="user_content">
				   <img  class="user_logo" src="https://thirdwx.qlogo.cn/mmopen/vi_32/DYAIOgq83epgbNJDsHrP7KEyiaaGGz6HnGbaAJicgdWl46OAm1BHYrUfiadyzcfjsbmsYz35RExCuTDHV8YQ0YEtg/132" /> 
				   <view  class="u_l_1">
				    <view  class="u_l_p1">ID:吴小双Jacky</view> 
				    <view  class="u_l_p2">已使用食图图的第90天</view>
				   </view> 
				   <view  style="clear: both;"></view> 
				   <view  class="use_m_l">
				    <img  src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACoAAAAvCAYAAACVDljoAAACn0lEQVRYhe3ZTWtcVRjA8d+EeMNQrVhaa8Rm0Y0vsWu7qWkXKqhEcGEFaf0AGt2ZTuiuyLSQviAIbUDQoAtB8BWXgvQjNCgqFEoXgRg3uhgyxkwX9w4tMXPvOXfuZFLIH4a5wznPef7Mebnnnltbm51TESN4FHuz339jBRt5Qc16Etx4FbyMW1jGb9lnGbfxShUJqhB9Fd/jiS3KHsd3eK3fJP2KJlgoaGcE1zDWT6J+RZ/HeEC9gzjRT6Kyog/iA3wSEbOA2Sw2mjKi0/gdFzAREXcI5/GHEmM2RrSGD/GtsO7uxWP4Bs2szSBGIxJcwXuRUnmcwZ7QNkP/0ZnQBiOZabTaMyEVQ0QnMd+fTy7zjVZ7sqhSiOhl6Xo5KBJcKqpUJHocL1RhU8CLjVZ7Kq9Ckeg7FcoUkZsrT/QR6Zq5XUw3Wu2HexXmiU4Z7NjczJj0lrwleaLPVe9SyNFeBXmiTw1ApIgnexXkie4fgEgR+3oV5Ik+NACRIkqJ7ih2RatmV7RqdkWr5t5HkSM4JT2WIe7BrSomGq32p9n1Chab9WQJatnZ0+v4Utwz1HbwL04268nX3a6/audJwgP4mHSM1nBgqDr5jDda7VpXdKdTu29m/Qg6w5YIoNMV/XXYJjksNetJpzvTj+EtOfvBIbGKz7m7JP2Fj4Zhst1n+AMndJGfwmeDEGi02uea9aTwQDhU9Dr+wbN9Wf2fX2RjsIjQrt/Au6V1tqaFN5v1ZC2kcswY/Vl6HF4FG3gDN0IDYifTWfwYGbOZdZzGDzFBsaLr0i3hV5FxXVbxEr6IDSyzPK1Ju+196QQLoYNFPIOfSuQsvY52pDeIw5iTjrWt9gw3cRFP4238WTJf35vlVelrmO6rmNHsu4P/FLxZjuEOxNBvZWaX6lgAAAAASUVORK5CYII=" class="user_icon" /> 
				    <view > 剩余下载次数 <span  style="color: rgb(0, 157, 251);">33张</span></view>
				   </view> 
				   <view  class="use_m_r">
				    <img  src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADIAAAAxCAYAAACYq/ofAAADmUlEQVRogdWabWhOYRjHf9sw0/jGWsoYhklZPnhpHywheclbyUssVgoh+SCv+SQkCvNBJEtNEkVevngreWu0FFrClH1YXrc1Y9Z06Trr6TjneZ77nPs8z7N/PT1v51z39Tv3fe5zXdd9Z1H9HUsaA1QA5cA4oATI9zD9CWgA6oG7wH3gR1gXwoIUApXAamBsQBt/gBtADXBVvxsrKMhwYAewFugbEMBL74FDwBmg0+TEbMOGcoG9wGtgvWUI0QjglA67CpMTTUDGA8+B/UB/cx+NJPfYHeCEXjxrIMuAp0BpxABubQQeAkMTHZgMyBagFhhg3c3kNElhSuIdnQhkK3AsxY57qQh4AIz0OyAeyHLgaErcTE4FwG1gsNfRfiATgLNpdtxL0iMXvPz2AskDLqVgZgqqmfoMSwiyW8ONTNY+YHQ8EOm67ZYB3gDngZ8WbfbTZ0yP3CB79CBbkmBwMrAG2GzRrmgWMNULRKa4VZYb+wC06Oc6y7bRcOmfYkGqgJwIGnPUHYHN2doBPSBZEfRGKiR+r4wFmaiheW/U4liQGb0UQlQmzz4HpDzNzoSRMBQ7IKkOz21riANS3MtBCrL1zo9y2k2F8k1z9kxVntMjQfVE09FnIQGPAzuBtqAG+oR84i7Rgts54Lpp5UO1QSsnolyNbE3VFXZoDdP3dmCeVg6DQoiKAvrxK1t7pD2gAUnARulnUxg3hCRLlQH9+Ob0SENAA1KmuRcAxgviQEAfRM0OyMsQRkxhbEOImhyQOyEN+cHE2u2OCEIyz0aniF2kSVBYyQw2HXibhB0bEKJbwBynRxqBRxaMunvGT7YgRBdxZYg1lgwngrEJIUP4Mh4gXyw14AdjEwItIrbiAmnTUMGWHJhSDYN2WYaQhaDDzhf3itUgrUMVWmywC/istVubkrr0NseeO0Rpif3TknIigGhyx2ResVatcwNlsKqceyMeiGgd8C5DOQ4CN90/+oFIqXM+8DV6v4x0RSeN/xQvjH+lYUarWVuRSWK3FTp5GIGgT/sKnXXSKdlIMBfo8PMhmcSqTivq9WkCOQIsTbQskWyGKDf+FKA6omK0l5qBBbpe4zmcYmWS6nZooWEa8CIKz1Xi9Eldjr6W7ElBcvbHuva9yPKax2/gtG7O2WS6Y8jGNqcy3R20MEBFv1MvTK2+Ak/3NvdriWQNXK6oBIzyGqirxNLzcsVleMoMKAnYR43rfGeipAX8BeQDttEuFafnAAAAAElFTkSuQmCC" class="user_icon" /> 
				    <view > 已下载次数 <span  style="color: rgb(0, 157, 251);">17张</span></view>
				   </view>
				  </view>
			</view>
			
			<view class="down-box2">
				<view class="down-box2-content">
					<img src="https://admin.shitutu.com/public/baiduimg/dt1.png" alt="">
					无线下载
				</view>
				
				<view class="down-box2-content">
					<img src="https://admin.shitutu.com/public/baiduimg/dt2.png" alt="">
					批量解析
				</view>
				
				<view class="down-box2-content">
					<img src="https://admin.shitutu.com/public/baiduimg/dt3.png" alt="">
					高清图片
				</view>
				
				<view class="down-box2-content">
					<img src="https://admin.shitutu.com/public/baiduimg/dt4.png" alt="">
					专属客服
				</view>
			</view>
			
			<view class="downCard-content">
				<view class="downCard-content-box">
					<view class="downCard-content-title">
						请选择充值套餐
						<img src="https://admin.shitutu.com/public/baiduimg/right.png" alt="">
					</view>
					
					  <view  style="justify-content: space-between; width: 100%; display: flex; margin-top: 40rpx;">
					   <view  class="buy_card_box  selected">
					    <view  class="b_c_b_1">2张</view> 
					    <view  class="b_c_b_2"><span  style="font-size: 30rpx;">￥</span>9.9</view> 
					    <del  class="b_c_b_3">
					      ￥19.9 
					    </del> 
					    <view  class="b_c_b_4">立省10元</view>
					   </view>
					   <view  class="buy_card_box ">
					    <view  class="b_c_b_1">50张</view> 
					    <view  class="b_c_b_2"><span  style="font-size: 30rpx;">￥</span>189</view> 
					    <del  class="b_c_b_3">
					      ￥199 
					    </del> 
					    <view  class="b_c_b_4">立省10元</view>
					   </view>
					   <view  class="buy_card_box ">
					    <view  class="b_c_b_1">20张</view> 
					    <view  class="b_c_b_2"><span  style="font-size: 30rpx;">￥</span>99</view> 
					    <del  class="b_c_b_3">
					      ￥109 
					    </del> 
					    <view  class="b_c_b_4">立省10元</view>
					   </view>
					  </view>
					  
					  <view class="downCard-content-title" style="font-size: 28rpx;">
					  	支付方式
					  
					  </view>
					  
					  <ul  class="pay-wrapper-list">
					     <view  class="solid_border" style="width: 100%; margin-left: 0px; padding-bottom: 0px;"></view> 
					     <li  class="pay-wrapper-list-items">
					      <div  class="pay-wrapper-list-items-left">
					       <img  src="data:image/png;base64,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" class="payment-icon" /> 
					       <div  class="payment-title">
					        支付宝支付
					       </div>
					      </div> <img  src="data:image/png;base64,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" class="payment-select" style="" /> <img  src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAwCAYAAABXAvmHAAAABHNCSVQICAgIfAhkiAAABHlJREFUaIHNmltsFFUYgL9/uu1KKbXRRsVgbLRaEqg1InYx8ckXIljivdoHE0LQUIhQQdq1D21SuxVRNEZRAokBNWAiqcR4edBgoqFIguEiUhUQU1GSWrAWaHfZ/X2YbejeZmemO1O/tzPzn3O+f2dm58w5RygE7XorCeqBEMo9CPU5IvtQ+hAOkKCPHjk52a7Fdc1VGqSMpxBagLkuWzkKvMogH7BFYm4acJ7AWp1OCctQ1iLMctNpBsoA8AoxtrFRLjipaj+BDi1jjBUI64BKh4p2GQQ2UMJmOmTETgV7CYT1DmAPcLN7Nwcov1HEQrqkP1+okbexsC5C6cMveQChigTf06YN+UKtEwhrM8onCNMKJmefcmA3YX3OKij3LdSmqxE2FdrKFcoaIvJ6tlPZE3hRH0Tpxc4t5g8JlEeISG/6icwE2rWGBAeBUj/MbKP8QxH16Q926i/coeXE6eX/Jg8gXE2cXjq0fOLh1ASitCDM9lXMCcJsorSkHhqnTW8HDiME/fZyhDJGnGo2yABMvALCiqmUv246TAvYCBSCBFh5pQjQoRWMcWaK/u9ZPh/eWAwXonDnmzAwnLfKEJeYxSa5ZF6BGI1TJb90HryzBK4KwLWlELrJVrVrKOVpGL+FEjzrnWJuls6DrQ+BJJ/EPT/B7mM2KyedhXV6A8X86ZFjTtLlv/wFFm+HywkHjcSYaRAg5ImhBdnkG3Y4lAcIEDKABYUWtCKXfDTuqrkFBkJdAf0sKbA8CHUGUF0oQSsKLm9SbQBlk9ezxiN5gDIDpcIqwhB4vBbmXu+uBw/lQanIO97vvB92NcLhVdDk8GnxVD6JAYxaBcxIjo5EYMdj8Ogcew031Xkvj3DeQDhvFdPzDfyejBCBnY35k2iqM5P1VN5kxACOW0X8NQL3vgsnh8xykWEm0ZDjq8FHeYBfDZRD+aL+GM5M4uOmzCR8lgflkIHwg53Ys8kr0T9olgPJJBbeZpbT5b8+4bG8yT6hVaswOGW3RmUpfPsM1CQnF6Nx+OiImcBE+UXbYfSyF84TiDHT7DKsR3Aww1xZCnuXwZws7wbf5OEo3VJrvgeUbU5qDl6E+7bAj2dTj/soD8JbMP5BE+Q9YMhJ/XOjZhIHz5jlr/yUV85RzIcwcVYirD3AeqdtlQfhrhvhu9MQczqed8/LdEsrpM5KbHbT0vAY7D3lq3yK65UEXpLTQKePGm7pTLoC2eZGw3ocqPHTyDbKMSKSMpDJHI0aLAEu+uVkG3Ny9+H0w5kJdEk/yhO+SDlBeDLbklP274GIfIqyxnMpuyRopls+z3Yq9weNuSKyGsXb0YwVZt8r6ZG3c4XkX6Vs0weAnQgzCqiWH+VfoJGIfGYVZm+ZtV1riPMFQlUh3GzQj9JARH7OF2hvDaxL+glSC7yAuRjtFYMo6ynhbjvy4HarQTHNyT0SLucq0lAGEDYSZat3Ww3SWa7FVNIEPM9kNnsor/E37/u32SMbrXoLBiGU+QghyDFhrOwH9iEcwGA/XXJisl3/B+fOd/mz8mBFAAAAAElFTkSuQmCC" class="payment-select" style="display: none;" /></li> 
					     <li  class="pay-wrapper-list-items">
					      <div  class="pay-wrapper-list-items-left">
					       <img  src="data:image/png;base64,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" class="payment-icon" /> 
					       <div  class="payment-title">
					        微信支付
					       </div>
					      </div> <img  src="data:image/png;base64,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" class="payment-select" style="display: none;" /> <img  src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAwCAYAAABXAvmHAAAABHNCSVQICAgIfAhkiAAABHlJREFUaIHNmltsFFUYgL9/uu1KKbXRRsVgbLRaEqg1InYx8ckXIljivdoHE0LQUIhQQdq1D21SuxVRNEZRAokBNWAiqcR4edBgoqFIguEiUhUQU1GSWrAWaHfZ/X2YbejeZmemO1O/tzPzn3O+f2dm58w5RygE7XorCeqBEMo9CPU5IvtQ+hAOkKCPHjk52a7Fdc1VGqSMpxBagLkuWzkKvMogH7BFYm4acJ7AWp1OCctQ1iLMctNpBsoA8AoxtrFRLjipaj+BDi1jjBUI64BKh4p2GQQ2UMJmOmTETgV7CYT1DmAPcLN7Nwcov1HEQrqkP1+okbexsC5C6cMveQChigTf06YN+UKtEwhrM8onCNMKJmefcmA3YX3OKij3LdSmqxE2FdrKFcoaIvJ6tlPZE3hRH0Tpxc4t5g8JlEeISG/6icwE2rWGBAeBUj/MbKP8QxH16Q926i/coeXE6eX/Jg8gXE2cXjq0fOLh1ASitCDM9lXMCcJsorSkHhqnTW8HDiME/fZyhDJGnGo2yABMvALCiqmUv246TAvYCBSCBFh5pQjQoRWMcWaK/u9ZPh/eWAwXonDnmzAwnLfKEJeYxSa5ZF6BGI1TJb90HryzBK4KwLWlELrJVrVrKOVpGL+FEjzrnWJuls6DrQ+BJJ/EPT/B7mM2KyedhXV6A8X86ZFjTtLlv/wFFm+HywkHjcSYaRAg5ImhBdnkG3Y4lAcIEDKABYUWtCKXfDTuqrkFBkJdAf0sKbA8CHUGUF0oQSsKLm9SbQBlk9ezxiN5gDIDpcIqwhB4vBbmXu+uBw/lQanIO97vvB92NcLhVdDk8GnxVD6JAYxaBcxIjo5EYMdj8Ogcew031Xkvj3DeQDhvFdPzDfyejBCBnY35k2iqM5P1VN5kxACOW0X8NQL3vgsnh8xykWEm0ZDjq8FHeYBfDZRD+aL+GM5M4uOmzCR8lgflkIHwg53Ys8kr0T9olgPJJBbeZpbT5b8+4bG8yT6hVaswOGW3RmUpfPsM1CQnF6Nx+OiImcBE+UXbYfSyF84TiDHT7DKsR3Aww1xZCnuXwZws7wbf5OEo3VJrvgeUbU5qDl6E+7bAj2dTj/soD8JbMP5BE+Q9YMhJ/XOjZhIHz5jlr/yUV85RzIcwcVYirD3AeqdtlQfhrhvhu9MQczqed8/LdEsrpM5KbHbT0vAY7D3lq3yK65UEXpLTQKePGm7pTLoC2eZGw3ocqPHTyDbKMSKSMpDJHI0aLAEu+uVkG3Ny9+H0w5kJdEk/yhO+SDlBeDLbklP274GIfIqyxnMpuyRopls+z3Yq9weNuSKyGsXb0YwVZt8r6ZG3c4XkX6Vs0weAnQgzCqiWH+VfoJGIfGYVZm+ZtV1riPMFQlUh3GzQj9JARH7OF2hvDaxL+glSC7yAuRjtFYMo6ynhbjvy4HarQTHNyT0SLucq0lAGEDYSZat3Ww3SWa7FVNIEPM9kNnsor/E37/u32SMbrXoLBiGU+QghyDFhrOwH9iEcwGA/XXJisl3/B+fOd/mz8mBFAAAAAElFTkSuQmCC" class="payment-select" style="" /></li>
					    </ul>
						
						  <view  class="pay-btn">
						   立即支付
						  </view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				pic_url:'https://admin.shitutu.com/public/baiduimg/downVip.png',
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
