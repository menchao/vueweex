<template>
	<view style="background-color:#999999">
	asgd 
	</view>
</template>

<script>
	export default {
		 data() {return {num: 1}},
		        created() {console.log('页面created')},
		        methods: {
		            changeNum() { this.num += 1; },
		            showModal(type) {
		                if (type === 'uni') {
		                    uni.showModal({content: '使用 uni-app 的 API 弹出模态框'});
		                }
		                else if (type === 'plus') {
		                    plus.nativeUI.alert('使用 uni-app 的 API 弹出模态框');
		                } else {
		                    var modal = weex.requireModule('modal')
		                    modal.alert({message: '使用 weex 的 API 弹出模态框'});
		                }
		            }
		        }
	}
</script>

<style>
	  .example {flex-direction: column;}
	    .text {line-height: 80px;font-size: 32px;color: #333;}
	    .item {height: 80px;width: 690px;margin: 30px;background-color: #f8f8f8;border-width: 1px;border-color: #eee;border-radius: 10px;align-items: center;}


</style>
