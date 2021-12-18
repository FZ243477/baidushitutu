<template>
	<view>
		<view  class="indexBody" :style="'min-height:'+swiperHeight+'px'" >
			<view class="liuhaiclass" :style="'height:'+liuhaiHeight+'px'"></view>
			<view class="title">图片详情</view>
			<view class="detail-content">
				<view class="detail-img-box">
					<img src="https://image.shitutu.com/uploads/20210105/99f38c0d550522a5c10d0a50cf00107a.jpg_logo" alt="">
				</view>
			</view>
			
			 <view  class="detail_img_content">
			   <view  class="de_box_1">
			    <view  class="de_l">购买授权:</view> 
			    <view  class="de_3">图片版权授权期为自下载之日起一年</view>
			   </view> 
			   <view  class="de_box_2">
			    <view  class="de_l">图片类型:</view> 
			    <view  class="de_3">JPG1250&times;1872</view>
			   </view> 
			   
			   <view  style="clear: both;"></view> 
			   <view  class="de_box_3">
			    <view  class="de_l">图片ID:</view> 
			    <view  type="number" class="de_3">STT159480273409884</view> 
			    <view  class="de_l">版权所有:</view> 
			    <view  class="de_3">食图图</view>
			   </view> 
			   <view  class="de_box_4">
			    <view  class="de_l">授权范围:</view> 
			    <view  class="de_3">可做商用、个人</view>
			   </view> 
			   <view  class="de_box_5">
			    <view  class="de_4_box">
			     <view  class="de_4">收藏</view> 
			     <img  src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAC4AAAAsCAYAAAAacYo8AAAEeElEQVRYhc2Za4hWRRjHf/vuZtkuKtpFrDRLhHBbbQNNukg3sSSqD1ZQQUkUhNEFoaLI6kMqlFFUuGS3LwZ9SSVKKoKIij6oa20UluvWJhVZdnXxkm888J98OJzznnP2zLvrHw4z55w58/znOTPP/GempaenhyahRdXWm1F9rQl1LgK+AA7r+h64PbaRtsj1LQY2JRxyGmC/tQNYE8tQTI+PAV5QnUPAg8Ay4Ge9fxw4IZaxmMSXAlOVXw6sAp4HbtWzdj2PgljE2xypQWCde/cO8Jnyy2J5PRbxm4AzlX8COJB4/6hS8/pdMQzGIG7eflj53cDLKWU2O6/fDUyoajQG8Rudt59M8XbASqXjgXuqGq1K3L6/X/mfFPayYGGyV++M+LiqhqvgOuAsfb9aYTALNoM+pnfm9TtHi7h9+4jyv+R4O2AjR7y+XJPSsI2XhQ2sBfJw8PaaHG8H1PWdYRLwHLAQmFKWRCOR1QrMAGYDXS6dmij3K3A68HdBm+asPtfogN+kccLVp+vPtEq8VrEKr5FImgN0AmNzSPwOrChBGgmvh4C1wEnu+UT9yQWJ8t8BnwPvAq8GW8HjNsLfAi5sYGyHKtju0sEShNNwInC2/mSnu9ozyvcDlwIDwePPONLWoi0Jgl8W7MNlYYP6A10BpuOnq0GdSufq2RnAS0Y+EL9Z6fvA1cC+JpAsiro8268ohBqzTkLuEht/NfXtVhVYO8qks2CNecW9a6slllZzjw6eqZjnHh4OxD/SA5sUbjlKiHpc77TOt8DBMAHdq8FX0y+pLIIi4jZgPXCMEQbuwM2cFkUud8H+aY7oitHEfcCLbjm4OEQgP+V/DFwE7NG96ZBn3TbDSMMWH0/Jpjn0MuC9wCGpVSxmz9eWAlqtvOaizkigRX98hWzt0Wz6ibedJrKs858PfK17i/FvAseNAOlWxeswxnZrYuxNFsxShz+o22zR/VXA21XFfw5se+N1TTKGncAFzoGFiKPp2HTBh7q/WH0sS0dUxQZgierok6cHsurM0+N/AFdq4Bq6gUNNIj5L6Tdy0o+NChdZSOxzsvUrYH91jqnYrof/usiWiaIroG6lW5tEGkd8JnB8XuEixE+RbqbJxEPkqEnONkQR4t0uvy0+3//hQ96cvMJFiJ+jtJ4WTyOi342lqMQtrv7VROJ1189n5xUuQvxcpWX7d8cwdmYD8a48bnnEJ+pEgRL92wg/oMljQPvkRRsQiHdofZmJPOJ+YOZ53BNeqQ2fdu0tFm1A4QGaR7zL5bM8PkESdNARRpNV2Fou2oBw6IVW98MmHkTVAe00pREekAQNe969WmpZLD4PuKJEA4ZcABhfhXhQZmPCkimFcDBghK9V93rDeW5ziQYsdfXtaEQs74B2rCo4Vfe7gJMTU3KvlnkbCx7GLlLD/ap9v7baZup+rw4L9mZVkufxIe2BhwqmO9LewxtKnCCn/YFjHel/gBsakTYUOaD9FJgmY5OlFm0QmfysctxtDbAr7AhbF7QzUZPQDUkD/AdHHvwLUAFq4AAAAABJRU5ErkJggg==" alt="" class="de_4_img" /> 
			     <view  style="clear: both;"></view>
			    </view> 
			    <view  class="de_4_box">
			     <view  class="de_4">举报</view> 
			     <img  src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAC0AAAAtCAYAAAA6GuKaAAAEZElEQVRYhc2ZT4hVVRzHP++OBQOjTm5c6bRxRMIpcyG5EWwhBTFGUDhhBAlBIGShYEMOJuYiqIUgDAQpw4y1iHQVbQbcNLgQJRFRN42t3Mg4TTwiZl6c4fsbfu/47rt/Z+oDl8e5957f7/vOPed3zvmdxvj4OBXoAXYBrwIvA9uBrcAGPVsE5oGHwD3gBjAN3NSzUqwrWW8HcAR4F9jc5b0g/DldLwJv6/4jYBL4Frhb1HlS8P0h4CfgDvBJhuBubFb9O7I3VKRy3pbuA84AR9V6MY+Ba8Bt4AHwBPgTWA9sBLYBO4F9wCZXtwEcBN4AzgOfAwt1iH4J+AEYjO4H4xO6rgNLOWyFL7sHOKyrT/dDQ3wMvA68A9zKMtKN0Aq/RoKbwBfAFuAjYCanYPTejOptkZ2mez4ofwfLig4t8SPQ6+79okE4BszlFJrGnOzskF2jV34PFxUd/unF6Pko8BowW1FszKzsjka6Lqa1eCfRoQ9PuWf/AIeAL4FWzYKNluyPyJ9pm5KeNuKB2KdB57vEe8D3BQTs1wRjhIllOmfdy/qd0m+v9Oz2USVu6TPRoBstKDjwAfCdu0K5CJejrjIoXSt40UOKw0YYHOcKCsZ93rRyHs5Fg/Oon4C86NNu4ghh6MOSfbiZUc5DS/6tbo/0tYkOYWfYGfuqQpT4O6Ocl1npMIalc0X0EU2pqMN/U9JRnaKRDhuADelcFt2j1ZoxUXHiqKN7GHPSYwSdPYnWw361NpFqIh91DESP1xN07kq0gDcea/FThb+iunG5KNely9ifaMdhXCuw+Ekj3pGU3qGIJekydifaIhm3KwpG6+hu5TJ4XduTaMp9UIODOLbXsV7xurYm2oQaT6rbf8pG3TY3JNH2qY5PuRp4Xcshzw+U9TU4jGN81c0Cka7FRHkJY2N1+6uC1zWfaL1rbKvB43xGuQxe18NEmR9jZw0O4jhfNe4T6bqXKFVl7CuRwImZ0wrNrqp9OpEu48Y62rdCm5SXmKng5Hfg+Wo629gTJXimEyUDH7mbqVv3/wivJ+i8aSFvMhLd/z8R3B+JnrSQh7KXNt2GHfmxCo5G1I/tCuWyHHOps5Z0rgy6kG696gwfBwZKOnpWcdWuUC7DgHQYVy0t7CPFmJsdQ75h3G3B1pqG/Fv+ZVH6iEX/pnSrcQA4WULsQhTyMlO3HTgp/8Z56VsmPr7oU9z2CZsRl/lZCw65DFPgflaGaUH5Yb8ZvSRDayX4kis3pafta3Wa/W6pdW36fUb//LNV7OMN2Z+SP+R/pFOCPW3KvgK8H60bzgI/V4gqaQzI7ln3fEn+r3Sq022dEbbub0Vd5YDCzukaJqB+2bkbDbqm/KamMrIWR+Gf7tVgMEIYOgX8AVwAXimwyEr0/gXVPxWlle/LX8cWNvIefq7W6ZaxWOR0q+iJ7ZA+6XBNg7KlmW7Mx+Esiq6dg+E3gReAr6PVYRFCvVA/2An2cgsOlD1mDoPnU+DEmp+NA/8Cd58PzFCzOs8AAAAASUVORK5CYII=" alt="" class="de_4_img" /> 
			     <view  style="clear: both;"></view>
			    </view>
			   </view> 
			   <view  id="qrcode" title="https://shitutu.com/activityDetail?id=11028" style="display: none;">
			    <canvas  width="200" height="200" style="display: none;"></canvas> 
			    <img  alt="Scan me!" src="data:image/png;base64,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" style="display: block;" />
			   </view> 
			   <view  style="clear: both;"></view>
			 
			  
			  <view class="solid_border" ></view>
			  
			  <view class="go-down-box">图片下载</view>
			  <view class="go-buy-box">购买下载卡</view>
			  
			    <view class="solid_border" ></view>
				
				<view class="more-title">相似图片</view>
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
