<script>
	export default {
		globalData:{
			isDark:true,
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
		},
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	

	/*每个页面公共css */
</style>
