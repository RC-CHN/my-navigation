<template>
	<view class="content">
		<view>
			<image src="../../static/logo.png" class="logo"></image>
		</view>
		<view class="search-bar">
			<input class="search-bar-input" autofocus="autofocus" placeholder="搜索一下..."
				placeholder-style="font-family: 'Jetbrains Mono';" v-model="searchText" @input="searchLog">
		</view>
		<view class="buttonBox">
			<button class="search-bar-button" style="" @click="searchBing">Bing</button>
			<button class="search-bar-button" @click="searchBaidu">Baidu</button>
		</view>
		<view class="nav-panel">
			<urlItem v-for="content in sites" v-bind:content="content"></urlItem>
			<!-- <view class="nav-panel-item" title="Bilibili" href="https://www.bilibili.com/" target="_blank">
			        <image src="https://www.bilibili.com/favicon.ico" alt="Bilibili" height="16" width="16" class="nav-panel-item-img">
			        <view class="nav-panel-item-txt">Bilibili</view>
			    </view> -->
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				searchText: "",
				sites: [{
						'url': "https://cas.hdu.edu.cn/",
						'title': '数字杭电',
						'icon': '../../static/web_icons/HDU.png'
					},
					{
						'url': "https://gitee.com",
						'title': 'Gitee',
					},
					{
						'url': "https://github.com/",
						'title': 'Github',
					},
					{
						'url': "https://www.bilibili.com",
						'title': "Bilibili"
					},
					{
						'url': "http://m.rcfortress.site:996/#/",
						'title': "ybb计算器",
						'icon': "../../static/favicon.png"
					},
					{
						'url': "http://m.rcfortress.site:81/login",
						'title': "Unraid管理页面",
						'icon': "../../static/web_icons/unraid.png"
					},
					{
						'url': "http://m.rcfortress.site:5000/",
						'title': "群晖-杭州",
						'icon': "../../static/web_icons/DSM.png",
					},
					{
						'url': "https://nas.rcfortress.site:5001/",
						'title': "群晖-湖州",
						'icon': "../../static/web_icons/DSM.png"
					},
					{
						'url': "http://m.rcfortress.site:9080",
						'title': "Gitlab",
					},
					{
						'url': "http://m.rcfortress.site:8443/login",
						'title': "CodeServer",
						'icon': "../../static/web_icons/code.png"
					}
				]
			}
		},
		onLoad() {},
		methods: {
			searchLog() {
				console.log(this.$data.searchText)
			},
			searchBing(){
				let searchUrl = "https://cn.bing.com/search?q=" + this.$data.searchText
				window.open(searchUrl);
			},
			searchBaidu(){
				let searchUrl = "https://www.baidu.com/s?wd=" + this.$data.searchText
				window.open(searchUrl);
			}
			

		}
	}
</script>

<style>
	.buttonBox{
		margin-bottom: 40rpx;
	}
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		font-family: 'Jetbrains Mono';
	}

	.logo {
		width: 560rpx;
		height: 200rpx;
		margin-top: 70px;
	}

	.search-bar {
		margin-top: 25px;
		width: 600px;
		height: 100px;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: -100rpx;

	}

	.search-bar-input {
		width: 580px;
		height: 25px;
		padding: 9px 10px;
		font-family: 'Microsoft YaHei UI', arial, sans-serif;
		font-size: 15px;
		color: #555;
		border: none;
		background: #fff;
		overflow: hidden;
		outline: none;
		vertical-align: middle;
		border-radius: 2px;
		background-color: rgb(222, 222, 222);
	}

	.search-bar-button {
		margin-top: 20px;
		margin-left: 20px;
		width: 105px;
		height: 35px;
		overflow: hidden;
		text-align: center;
		font-size: 15px;
		font-weight: bold;
		color: rgb(255, 255, 255);
		border: none;
		overflow: hidden;
		vertical-align: middle;
		outline: none;
		cursor: pointer;
		border-radius: 5px;
		background-color: rgb(20, 162, 245);
		display: inline-block;
	}

	.search-bar-button:hover {
		background-color: rgb(30, 172, 245);
		box-shadow: 0px 0px 3px rgb(242, 242, 243);
	}

	.nav-panel {
		margin-top: 20rpx;
		/* margin-bottom: 100px; */
		width: 80%;
		min-height: 600rpx;
		margin-left: auto;
		margin-right: auto;
		padding-left: 30px;
		padding-top: 10px;
		background-color: rgb(58, 58, 62);
		border-radius: 10px;
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
		justify-content: flex-start;
		gap: 10rpx;
	}
</style>
